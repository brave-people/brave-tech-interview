# 네트워크

<br />

---

### HTTP 메소드에 대해서 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

[ CRUD 관점에서 설명해야함 ]
Create(생성), Read(읽기), Update(갱신), Delete(삭제)

- **POST :** 서버나 특정 리소스에 엔티티를 제출할 때 사용합니다. Create나 Update, Delete등을 할 때 사용하기도 합니다. [Create]
- **GET** : 특정 리소스의 참조를 요청합니다. CRUD를 예로 들 경우 R에 해당합니다. url에 어느 리소스를 참조 요청하는지 드러나게 됩니다.[Read]
- **PUT**: PUT를 통해 해당 리소스를 수정합니다. UPDATE를 하지만 전체 자원을 업데이트 하는데 쓰인다고 합니다. [Update]
- **DELETE** : 삭제 할 때 사용. 어느 자원을 삭제할 지 url에 드러나게 됩니다.[Delete]
- **PATCH**: 리소스의 부분을 수정하는데 사용합니다. 의미론적으로 UPDATE와 더 가깝다고 할 수 있습니다.

HTTP Request Method
GET : 특정 리소스의 참조를 요청합니다. CRUD를 예로 들 경우 R에 해당합니다. url에 어느 리소스를 참조 요청하는지 드러나게 됩니다.
POST: 서버나 특정 리소스에 엔티티를 제출할 때 사용합니다. Create나 Update, Delete등을 할 때 사용하기도 합니다.
PUT: UPDATE를 하지만 전체 자원을 업데이트 하는데 쓰인다고 합니다.
DELETE: 삭제 할 때 사용. 어느 자원을 삭제할 지 url에 드러나게 됩니다.
PATCH: 리소스의 부분을 수정하는데 사용합니다. 의미론적으로 UPDATE와 더 가깝다고 할 수 있습니다.

</details>

---

<br />

---

### HTTP1.1 vs HTTP2.0

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

**HTTP(HyperText Transfer Protocol)**

WWW(World Wide Web)에서 하이퍼텍스트(hypertext) 문서를 교환하기 위하여 사용되는 통신규약이다.

**HTTP/1.1**

Connection당 하나의 요청을 처리 하도록 설계 되어 있다. 그래서 동시전송이 불가능하고 요청과 응답이 순차적으로 이루어 지게된다. 그렇다 보니 HTTP문서안에 포함된 다수의 리소스 (CSS, JS, Images)를 처리하려면 요청할 리소스 개수에 비례해서 Latency(대기 시간)는 길어지게 된다.

**HTTP/1.1 단점**

- HOL(Head Of Line) Blocking – 특정 응답의 지연
- RTT(Round Trip Time) 증가
- 무거운 Header 구조 (특히 Cookie)

**HTTP/2.0 장점**

- **Multiplexed Streams**
  - 한 커넥션으로 동시에 여러개의 메세지를 주고 받을 있으며, 응답은 순서에 상관없이 stream으로 주고 받는다. HTTP/1.1의 Connection Keep-Alive, Pipelining의 개선이라 보면 된다.
- **Stream Prioritization**
- 예를 들면 클라이언트가 요청한 HTML문서안에 CSS파일 1개와 Image파일 2개가 존재하고 이를 클라이언트가 각각 요청하고 난 후 Image파일보다 CSS파일의 수신이 늦어지는 경우 브라우저의 렌더링이 늦어지는 문제가 발생한다. HTTP/2의 경우 리소스간 의존관계(우선순위)를 설정하여 이런 문제를 해결하고 있다.
- **Server Push**
  - 서버는 클라이언트의 요청에 대해 요청하지도 않은 리소스를 마음대로 보내줄 수 도 있다.
  - 클라이언트가 HTML문서를 요청했고 해당 HTML에 여러개의 리소스(CSS, Image…) 가 포함되어 있는경우 HTTP/1.1에서 클라이언트는 요청한 HTML문서를 수신한 후 HTML문서를 해석하면서 필요한 리소스를 재 요청한다.
  - HTTP/2에선 Server Push를 이용하면 클라이언트가 요청하지도 않은 (HTML문서에 포함된 리소스) 리소스를 Push 해주는 방법으로 클라이언트의 요청을 최소화 해서 성능 향상을 이끌어 낸다.
  - 이를 PUSH_PROMISE 라고 부르며 PUSH_PROMISE를 통해서 서버가 전송한 리소스에 대해선 클라이언트는 요청을 하지 않는다.

Source. [Link](https://www.popit.kr/%EB%82%98%EB%A7%8C-%EB%AA%A8%EB%A5%B4%EA%B3%A0-%EC%9E%88%EB%8D%98-http2/)

</details>

---

<br />

---

### URL 에 www.example.com 을 쳤을 때 일어나는 일들을 설명하세요.

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- http://owlgwang.tistory.com/1
- https://deveric.tistory.com/97
- [velog](https://velog.io/@jay/%EC%A3%BC%EC%86%8C%EC%B0%BD%EC%97%90-velog.io%EB%A5%BC-%EC%9E%85%EB%A0%A5%ED%96%88%EC%9D%84%EB%95%8C-%EB%AC%B4%EC%8A%A8-%EC%9D%BC%EC%9D%B4-%EC%9D%BC%EC%96%B4%EB%82%A0%EA%B9%8C-1-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)
- https://devjin-blog.com/what-happen-browser-search/

</details>

---

<br />

---

### 사용자가 웹브라우저를 통해 서버에 이미지를 요청해서 사용자에게 보여주기까지 과정을 설명하세요

<details>
   <summary> 참고 링크 보기 (👈 Click)</summary>
<br />

- 참고 [Link](https://krksap.tistory.com/1148?category=755546)

</details>

---

<br />

---

### HTTP와 HTTPS의 차이를 설명하세요.

<details>
   <summary> 참고 링크 보기 (👈 Click)</summary>
<br />

- 참고: [Link](https://post.naver.com/viewer/postView.nhn?volumeNo=16561296&memberNo=1834)

</details>

---

<br />

---

### HTTP 프로토콜의 특징

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 비연결 지향(Connectionless) : 클라이언트가 request를 서버에 보내고, 서버가 클라이언트에 요청에 맞는 response를 보내면 바로 연결을 끊는다.
- 상태정보 유지 안 함(Stateless) : 연결을 끊는 순간 클라이언트와 서버의 통신은 끝나며 상태 정보를 유지하지 않는다.

</details>

---

<br />

---

### 쿠키와 세션의 필요성

<details>
   <summary> 예비 답안 보기 (👈 Click)</summary>
<br />

- 쿠키와 세션의 차이
  - 세션은 서버에 저장되고, 쿠키는 클라이언트에 저장된다고 하셨는데, 그럼 쿠키가 안되는 상황에서도 세션은 사용할 수 있나요?
- 참고 : https://github.com/WeareSoft/tech-interview/blob/master/contents/network.md

</details>

---

<br />

---

### HTTP2의 특징을 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### 쿠키와 세션은 언제 사용하나요?

> 답안 준비중입니다.

---

<br />

---

### HTTP 응답코드에 대해서 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### OSI 7 Layer에 대해서 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### DNS에 대해서 설명하세요.

> 네트워크 통신을 위해서는 ip 주소가 필요하다. 인터넷 내의 모든 네트워크 장치 및 서버에는 이 ip주소가 할당되어 있다. 때문에 특정 서버로 데이터 요청을 하기 위해서는 ip주소가 필요하다.

일반적으로 ip 주소는 xxx.xxx.xxx.xxx 형식으로 이루어진 IPv4 형식을 많이 사용한다.

하지만 일반인이 이 주소를 모두 달달 외우고 있기란 쉽지 않은 일이기 때문에, 조금 더 인간에게 익숙한 언어형태를 통해 ip주소 대신 DNS(Domain Name System)을 사용하게 되었다.

DNS를 사용하여 특정 도메인 주소(www.google.com)를 브라우져 url 창에 입력하면, 브라우저는 Domain Name Server에 해당 도메인과 매핑되는 ip 주소를 요청하게 된다.

도메인 주소는** www.google.com** 과 같은 형식을 일반적으로 갖게 되는데,

- www : **Third-level Domain**
- google : **Second-level Domain**
- com : **Top-level Domain**
- 숨겨진 루트 도메인 (여기서 부터 시작)

로 구분된다.

도메인을 이렇게 여러 레벨로 찢어놓은 이유는 세계의 방대한 Domain 내용을 한 서버에 담아둘 수 없어 분산시키기 위해서이다.

브라우저는 도메인 요청이 일어나면 가장 먼저 로컬의 캐시 영역부터 해당 IP 주소를 찾기 시작한다. 캐시에 해당 주소가 없다면 DNS 서버에 쿼리를 하고, 결과를 반환받으면 로컬 캐시 영역에 저장해준다.

DNS 서버는 요청 받은 도메인이 DNS 서버 로컬 캐시에 존재하는지 다시 확인한다.

만약 없다면, DNS 서버에서는 해당 도메인의 IP를 찾기 위해서 루트 도메인부터 찾기 시작한다. 해당 도메인을 찾기위해 DNS 서버는 root NS(name server) 로 쿼리를 보내고, 이를 통해 .com(Top-level Domain 이하 TLD)의 NS 정보를 받아온다.

이 TLD NS 정보를 통해 이 정보에 해당하는 TLD NS에 다시 google.com 에 대한 정보를 쿼리하게 된다. 이렇게 되면 google.com 의 IP주소가 있는 네임서버를 반환 받게 되고, 편의상 goo네임서버 라고 칭하겠다.

DNS 서버는 이 goo네임서버로 google.com 의 정확한 IP 주소를 쿼리하게 되고, 해당 IP주소를 응답받게 된다. DNS 서버는 이 내용을 로컬 캐시에 저장하고 클라이언트에게 IP주소를 반환해준다.

---

<br />

---

### Web으로 Server Push를 구현할 때 제약사항 등을 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### 3 way hand shake에 대해서 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### 4 way hand shake에 대해서 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### 흐름제어, 혼잡제어방식에 대해서 설명하세요.

> 답안 준비중입니다.

---

<br />

# 🔥 Challenge

<br />

---

### 웹 사이트를 제작했는데 고해상도 이미지를 많이 사용하여 페이지 로딩 속도가 느립니다. 최적화 하는 방법에 대해서 모두 설명하세요.

> 답안 준비중입니다.

---

<br />

---

### 브라운이 새로운 검색 엔진을 개발하려고 합니다. 어떻게 설계 및 개발 것인지 아는 지식을 모두 동원하여 설명하세요.

> 답안 준비중입니다.

---

<br />
<br />
<div align=center>
  <hr />
    <h3> 용감한 친구들 with 남송리 삼번지 </h3>
  <hr />
</div>
