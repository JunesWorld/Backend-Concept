# Backend-Concept

## Internet vs internet
- internet : Network의 집합
- Internet : Header 내용이 같아 Data 통신이 가능 (거의 모든 Network의 Header는 같다)

## Packet = Header + Body
- Header : TCP/IP에서 정해 놓은 byte로 Data가 들어가 있고 이것으로 Data 통신
- Body(Data) : 응답 Body 만드는 것 (=Web programming)

## WWW(World Wide Web)
- HTTP가 거미줄 처럼 이어져 있는 것
- 문서끼리 연결되어 있다 = 프로토콜
	> naver -> news -> article

## URL(Unified Resources Location)
- 접근프로토콜://[IP주소] or [Domain 이름]/문서 경로/문서 이름
	> http://[192.168.0.10] or [www.naver.com]/hello.jsp

## HTML
- Hyper Text가 모여있는 것
- 어떻게 전달?
	- HTTP 사용
		1. Connect
		2. Request : Get방식(주소) / Post방식(Body에 정보를 숨김 -> Login)
		3. Response
		4. Close

## Tomcat

- Apache Tomcat -> Tomcat 9 (tar.gz) -> Download (나의 경로는 Downloads에 받았다)-> /Downloads/apache-tomcat-9.0.73/bin -> ./startup.sh(실행) // ./shutdown.sh(종료)
- Tomcat이란? 
    - 일종의 Program -> Servlet
    - Java를 실행하게 해주는 S/W
    - 일종의 Program -> Servlet
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
    - 상속(Inheritance) : 부모로 부터 물려받는 것 -> 확장성(Override)
    	- class <자식> extends <부모> { } 

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

## HTTP
- Server와 Client가 웹에서 데이터를 주고 받기 위한 프로토콜(규약)
- 특징(불특정 다수와 통신하기 위해)
	- 클라이언트 <-> 서버 모델
	- 무상태 프로토콜(Stateless) : 서버가 클라이언트 상태를 유지하지 않음 / 해결책 : Keep-Alive 사용
	- 비연결성(Connectionless) : 서버가 클라이언트 요청에 대해 응답을 마치면 연결을 끊어버림 / 해결책 : COOKIE(client에 정보 저장), SESSION(server에 정보 저장), JWT
- 응답코드
	- 2xx : 성공
	- 3xx : 리다이렉션 
	- 4xx : 클라이언트 에러
	- 5xx : 서버 에러

- 헤더 
	- Content-Type
	- Accept
	- Cookie
	- Authorization

## AWT(Abstract Window Toolkit)
- GUI를 구현하기 위함
	- Component(GUI 기능을 가지는 Class / Button, Checkbox)와 Container(Component들을 배치할 수 있는 Component / Frame)들을 가진 패키지
	- 운영체제에 종속적이지 않음

## JVM < JRE < JDK 
- JDK(Java Development Kit) : javoc, debugging, jar
	- Java Compile이라는 기능을 거쳐 기계가 이해할 수 있는 형태로 저장하는 기능 포함
	- Java 개발을 위한 필수적 도구들이 들어가 있다.

- JRE(Java Runtime Environment) : java, javaw, library
	- Java가 구동되기 위한 실행 환경 제공

- JVM(Java Virtual Machine) : just in time compiler
- Source Code < JVM(Java) < 운영체제(Window, Linux, OS) < H/W(Computer)

## Interface
- 추상 class가 확장성이 떨어지면 사용 : new 사용 x / Instance화 시키지 못하는 것 / Memory에 객체 생성 x
	> 주차시스템 -> parkable <- 자동차 = extends / 비행기 = implements

## 입출력(Input & Output)
1. File / Keyboard/ Network -> 
	> [Input : 입력 받는 역할을 하는 것 / 공통적인 class를 추상화(상속)(byte단위로 읽는다)]
2. 객체 생성 (변수, 데이터 타입) ->
3. Business Logic(DB) ->
4. Output ->
5. File / Console / Network
- Byte VS Character
	- Byte단위(Data 통신)
		- OutputStream // InputStream
		- [상속]
		- [주Stream] FileOuputStream / FilterOuputsTream // FileInputStream
		- [보조Stream] BufferedOutputStream
	- Char단위(Text)
		- Reader // Writer
		- FileReader / BufferedReader // InputThreadReader

## Spring
- 정의 : Java Enterprise 개발을 편하게 해주는 오픈소스 경량급 Application Framework

## Framework
- S/W를 만드는데 기본이 되는 골격 코드
- 완전한 Application S/W가 아니기 때문에(반제품) 확장하여 비지니스 요구사항에 맞는 완전한 Application으로 완성이 요구된다. 
- Framework를 사용해서 모든 플로우를 만들고 필요한 경우(Query 생성) 라이브러리를 사용

## Exception
- Unchecked Exception : Error
- Checked Exception : 찐 예외 -> try~catch 예외 처리
```
try {
...
} catch(e) {
	1. 사과
	2. 로그
	3. 정상종료
} finally {
}
```

## DataSource(Connection pool)
- Connection pool : DB에 미리 연결해 놓은 Connection 
- Apache Common DBCP : 가장 유명한 오픈소스 DB Connection pool libarary

## MyBatis(Library) = ORM(Object Relation Mapping) = JPA를 구현한 실체 => pom.xml에서 설정
- Memory에 있는 객체들을 어떻게 저장할까? -> RDBS / JPA(Java Persistence API) -> 가장 유명한 Library = Hibenate
- JPA -> ERD에서 One To Many 관계를 Class에서 어떻게 Mapping
	- Object <-> Relation : JPA(Hibenate) 
	- @Entity, @OneToMany...
- MyBatis = Object (Relation X) <-> SQL Mapping(Parameter & Result) => Mapper(XML, Interface)
- Session
	- Bean 설정 (Datasource, SessionFactory, SessionTemplate)
	- Session Factory는 DataSource를 주입 받아야 하고 Mapper(XML)로 SQL, Param, Result 바인딩 
	- session = sf.getSession() -> Session Template은 Session Factory 주입 받아야 한다.
		```
		1. 연결하기 = session.getConnection
		2. Transaction 시작
		3. Statement 준비
		4. 파라미터 바인딩
		5. Query 실행 / 처리
		6. Result 처리
		7. Transaction 종료
		8. 연결종료 
		```
	- Repository는 SessionTemplate 주입 받아야 한다. 

## Logging
- Non Functional Requirement
- 하지만,  프로그램 개발 중 디버깅 및 개발완료 후 문제점 추적 및 분석을 위해 필수적으로 갖추어야 할 요구 조건 
-  로그(Log)는  프로그램 개발이나 운영 시 발생하는 문제점을 추적 하거나  운영 상태를 모니터링 하는 정보
-  얻을 수 있는 것
	1. 재현하기 힘든 (테스트 환경이 아닌 개발 완료된 환경에서 발생하는) 버그에 대한 유용한 정보를 제공
	2. 성능에 관한 통계와 정보를 제공할 수 있다.
- 종류
	- Apache 의 (J)arkarta (C)ommons (L)ogging : Library에서 사용하기에 괜찮지만 Application에서는 X
		- info / warn / debug / error
	- Log4J : Application에서 사용하지만 잘 안씀
	- Slf4J(표준) : 인터페이스 / Logback -> 구현체
- Logger(Package 중심) <-> Appender(console & file)
	- debug -> info -> warn -> error
	- 개발자 = DEBUG / Release = WARN
- Rollingpolicy
	- 일정 용량 초과 시 zip 생성 

## Interceptor(접근 제어)
- /mysite03/...(url) -> url 제어해야함
- filters -> DispatcherServlet -> Interceptors -> Spring Container(Application(Controller1,2,3))
- Spring Security(Container)는 filters를 사용하지만 사실상 Spring Container안에 있다.
- Interceptor = Security
