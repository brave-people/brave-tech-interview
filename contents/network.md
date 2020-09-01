# 네트워크



### OSI 7 Layer에 대해서 설명하세요. 

### POST, GET, PUT, DELETE에 대해서 설명하세요.

[ CRUD 관점에서 설명해야함 ]
Create(생성), Read(읽기), Update(갱신), Delete(삭제)

- __POST :__ 서버나 특정 리소스에 엔티티를 제출할 때 사용합니다. Create나 Update, Delete등을 할 때 사용하기도 합니다. [Create]
- __GET__ : 특정 리소스의 참조를 요청합니다. CRUD를 예로 들 경우 R에 해당합니다. url에 어느 리소스를 참조 요청하는지 드러나게 됩니다.[Read]
- __PUT__: PUT를 통해 해당 리소스를 수정합니다. UPDATE를 하지만 전체 자원을 업데이트 하는데 쓰인다고 합니다. [Update]
- __DELETE__ : 삭제 할 때 사용. 어느 자원을 삭제할 지 url에 드러나게 됩니다.[Delete]
- __PATCH__: 리소스의 부분을 수정하는데 사용합니다. 의미론적으로 UPDATE와 더 가깝다고 할 수 있습니다.


### URL 에 www.example.com 을 쳤을 때 일어나는 일들을 설명하세요.


- http://owlgwang.tistory.com/1 
- https://deveric.tistory.com/97
- [velog](https://velog.io/@jay/%EC%A3%BC%EC%86%8C%EC%B0%BD%EC%97%90-velog.io%EB%A5%BC-%EC%9E%85%EB%A0%A5%ED%96%88%EC%9D%84%EB%95%8C-%EB%AC%B4%EC%8A%A8-%EC%9D%BC%EC%9D%B4-%EC%9D%BC%EC%96%B4%EB%82%A0%EA%B9%8C-1-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC)
- https://devjin-blog.com/what-happen-browser-search/

### 사용자가 웹브라우저를 통해 서버에 이미지를 요청해서 사용자에게 보여주기까지 과정을 설명하세요

- 참고 [Link](https://krksap.tistory.com/1148?category=755546)


### HTTP와 HTTPS의 차이를 설명하세요.

- 참고: [Link]( https://post.naver.com/viewer/postView.nhn?volumeNo=16561296&memberNo=1834)


### HTTP2의 특징을 설명하세요.


### 웹 사이트를 제작했는데 고해상도 이미지를 많이 사용하여 페이지 로딩 속도가 느립니다. 최적화 하는 방법에 대해서 모두 설명하세요.


### 브라운이 새로운 검색 엔진을 개발하려고 합니다. 어떻게 설계 및 개발 것인지 아는 지식을 모두 동원하여 설명하세요.


### 쿠키와 세션은 언제 사용하나요?


### 파생문제
- 쿠키와 세션의 차이
- 세션은 서버에 저장되고, 쿠키는 클라이언트에 저장된다고 하셨는데, 그럼 쿠키가 안되는 상황에서도 세션은 사용할 수 있나요?

--------------------

### HTTP 프로토콜의 특징

- 비연결 지향(Connectionless) : 클라이언트가 request를 서버에 보내고, 서버가 클라이언트에 요청에 맞는 response를 보내면 바로 연결을 끊는다.
- 상태정보 유지 안 함(Stateless) : 연결을 끊는 순간 클라이언트와 서버의 통신은 끝나며 상태 정보를 유지하지 않는다.

### 쿠키와 세션의 필요성

- 참고 : https://github.com/WeareSoft/tech-interview/blob/master/contents/network.md


### DNS에 대해서 설명하세요. 

- TODO


### Web으로 Server Push를 구현할 때 제약사항 등을 설명하세요.

- TODO


### 3 way hand shake에 대해서 설명하세요.

- TODO


### 4 way hand shake에 대해서 설명하세요.

- TODO


### 흐름제어, 혼잡제어방식에 대해서 설명하세요.

- TODO


