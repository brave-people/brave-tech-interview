# Day006 - 20.09.05

Topic: Operating System `#Cache` + RealWorld `#Redis`

__Question__ Cache의 3C misses에 대해서 설명하세요.
  
__Answer__
```
(1) Compulsory miss ; 데이터에 처음 접근 시 캐시에 데이터를 올릴 때 발생하는 캐시 미스
(2) Capacity miss ; 캐시 공간이 부족하여 생기는 캐시 미스
(3) Conflict miss ; 캐시에 공간은 있지만, 서로 다른 working set이 같은 캐시에 할당될 때 발생하는 캐시 미스
```
  
  
  
__+Real World Reading Article__ 컴퓨터를 적절한 가격을 주고 구매했다면 cache 때문에 고통받을 일은 없습니다. 그러나 Real world에서 Redis를 사용한다면 cache라는 주제로 고민하게 될 것입니다. [Brunch. Redis 기본 정리
](https://brunch.co.kr/@jehovah/20) 를 가볍게 읽어보고 간단히 Redis를 알아보세요.


__POP Quiz__ URL의 마지막에 `/`가 있을 수도 있고 없을 수도 있습니다. 둘의 차이는 무엇일까요?

```
https://www.hisnet.handong.edu/user/ 
https://www.hisnet.handong.edu/user 
```
  
   
__Answer__  
url의 마지막에 붙는 ‘/’는 trailing slash 입니다. 
슬래쉬가 있는 경우, 서버는 url을 파일로 간주하고 파일이 존재하지 않을 경우 디렉토리로 확인합니다.  
반대로 슬래쉬가 없는 경우, 서버는 url을 디렉토리로 간주하고 해당 위치가 없으면 404에러를 반환합니다.  
  
이 때, 구분해줘야 할 것이 슬래쉬가 url의 어디에 위치하는가 입니다.  
[scheme]/[host]/[path]로 구성된 url에서 trailing slash는 path의 끝에 위치합니다.  
hisnet.handong.edu/의 마지막 슬래쉬는 파일인지 디렉토리인지를 구분하는 구분자가 아니라 리소스 경로로 생각해야하고, 그 뒤의 경로인 user/의 슬래쉬가 리소스 종류 구분자가 됩니다.
