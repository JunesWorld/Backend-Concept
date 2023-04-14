# Backend-Concept

## Install Tomcat

- Apache Tomcat -> Tomcat 9 (tar.gz) -> Download (나의 경로는 Downloads에 받았다)-> /Downloads/apache-tomcat-9.0.73/bin -> ./startup.sh(실행) // ./shutdown.sh(종료)
- Tomcat이란?
    - Servlet Interface(Spac) 구현체
    - Servlet Container 중 하나 
        - 서블릿의 라이프 스타일 관리한다는 뜻

## Test Code

- TDD(Test Driven Development : 테스트 주도 개발)
    - 프로덕션 코드보다 테스트 코드를 먼저 작성하는 개발 방법
    - TFD(Test First Development) + Refactoring
    - 메소드 단위로 기능 동작을 검증
    - 흐름
        - Test fails -> Test passes -> Refactor

- BDD(Behavior Driven Development : 행동 주도 개발)
    - 시나리오 기반으로 테스트 코드를 작성하는 방법
    - 하나의 시나리오는 Given/When/Then 구조를 가짐

## 객체지향 페러다임
- 특징
    - 추상화(Abstraction) : 불필요한 부분 제거 / 복잡성 제거
    - 다형성(Polymorphism) : 다향한 형태를 가지는 것 / 하나의 타입으로 여러 객체를 참조하는 것
    - 캡슐화(Encapsulation) : 객체 내부의 세부 사항을 외부로부터 감추는 것 / 인터페이스만 공개해서 변경하기 쉬운 코드 만드는 것
    - 상속(Inheritance) : 부모로 부터 물려받는 것

- 원칙(SOLID)
    - 단일 책임의 원칙(Single Responsibility Principle) 
    - 개방 폐쇄의 원칙(Open/Closed Principle)
	- 확장 = open / 변경 = closed -> 기존 코드 변경하지 않고 추가할 수 있어야한다.
    - 리스코프 치환의 원칙(Liskov's Substitution Principle)
	-상위 타입 객체를 하위 타입 객체로 변경했을 때 동작에 문제가 없어야 한다.
    - 인터페이스 분리의 원칙(Interface Segregation Principle) 
	- 많은 기능을 가진 인터페이스를 작은 단위로 분리 시킴으로써 클라이언트에게 필요한 인터페이스들만 구현하도록 한다. 
	- 클라이언트가 사용하지 않는 기능에 의존하게 되면 예상하지 못한 문제가 생기는데 이 것을 예방 할 수 있다.
    - 의존성 역전의 원칙(Dependency Inversion Principle) 
	- 의존 관계를 맺을 때 변경이 자주 잃어나지 않는 곳에 의존해라.

- 적절한 객체에게 적절한 책임을 할당하여 서로 메시지를 주고 받으며 협력하도록 하는 것
- 점점 증가하는 SW 복잡도 낮추기 위함
- 클래스가 아닌 객체에 초점을 맞추는 것
- 객체들에게 얼마나 적절한 역할과 책임을 할당하는지가 중요

## 절차지향 VS 객체지향
- 절차지향 : 임이 한 곳에 집중되어 있는 방식(Getter)
- 객체지향 : 책임이 여러 객체로 적절히 분산 되어 있는 방식
	- High cohesion & Loose coupling(강한 응집도 & 낮은 결합도)
	- 어떠한 변경이 생겼을 때 다른 곳에 영향을 미치지 않는다 -> 유지보수와 관련!
