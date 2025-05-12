# 메모장 제작
: 메모를 CRUD 할 수 있는 Web Application

Layered Architecture 활용해 책임 분리


**순서**
 1. 책임 분리
    controller - 클라이언트의 요청을 받는 역할, 요청에 대한 처리를 Service Layer 에 전달, Service 에서 처리 완료된 결과를 클라이언트에 응답
    요청, 응답을 제외한 모두를 controller 에서 분리해야 함
 2. Service Layer 분리
    비즈니스 로직 수행
 3. Repository Layer 분리
    데이터 베이스와 상호작용


**layered architecture 만드는 방법**
1. controller 에서 메서드 추가하고, 그 이후에 Memo, Service, Repository 패키지 순으로 수정
2. 각 패키지에서 인터페이스를 먼저 수정하고, 그 인터페이스를 상속받은 클래스에서 @Override 해주는 방식
3. 예외처리도 추가 
