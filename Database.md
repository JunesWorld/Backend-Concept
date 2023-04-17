# Database의 기본 개념

## 정의
 * 여러 응용 시스템(프로그램)들의 통합된 정보들을 저장하여 운영할 수 있는 공용(share) 데이터의 집합

## 특성
1. 실시간 접근성
2. 계속적인 변화
3. 동시 공유성
4. 내용 참조

## 데이터 베이스 관리 시스템
 * (Database Management System = DBMS) -> Software(MySQL, Maria DB, ORACLE...)
 * 필수 기능
  1. 정의 : 데이터 베이스의 논리적, 물리적 구조를 정의
  2. 조작 : 데이터를 검색, 삭제, 갱신, 삽입, 삭제
  3. 제어 : 데이터베이스의 내용 정확성과 안정성을 유지하도록 제어

## 종류
 * 관계형 데이터베이스(RDB = Relatonal DB)
 > Key Value들의 간단한 관계를 테이블화 시킨 매우 간단한 원칙의 DB
 > 테이블로 구성되어 있고 여러 개의 Column(Key)이 포함된다.
 * 객체 지향 데이터베이스(OODB = Object Oriented DB)
 > 정보를 객체의 형태로 표현하는 DB
 > Data Model을 그대로 응용프로그램에 적용
 > 장점 : Data 변환 작업 필요하지 X
 * 객체 관계형 데이터베이스(ORDB = Object Relation DB)
 > RDB에서 사용하는 Data 확장
 > RDB를 객체 지향 모델링과 데이터 관리하는 기능 갖도록 확장한 것
 * NoSQL
 > 대용량 데이터의 웹 서비스와 SNS, 클라우드 컴퓨팅의 확대 보급과 대중화로 주목 받는 기술
 > 정형화 시키지 못하는 것 (SQL 사용하지 않는다)

## SQL(Structured Query Language) 개요
 * Database 스키마 생성, 자료 검색, 수정, 객체 접근 관리 등을 위해 고안된 언어
 * 다수의 Database 관련 프로그램의 표준 언어
 * 종류
  - DML(Data Manipulation Language)
    - 데이터 조작어로 검색 및 수정하기 위한 수단 제공
    > SELECT : 기본/통계/서브/*조인*
    > INSERT, UPDATE, DELETE = transaction
  - DDL(Data Definition Language)
    - 데이터 구조를 생성, 변경, 삭제 기능
    > CREATE, ALTER, DROP, RENAME
  - DCL(Data Control (Access) Language)
    - 데이터에 대한 권한 관리 및 트랜잭션 제어
    - 보안 = 인증 + 권한
    > GRANT, REVOKE

 * DA = Data Architecture -> Design
  - 정규화
   - 중복 없이 모여있는 것을 나누는 것 -> 어떠한 문제가 있기 때문!
   - 논리적으로 조직화 시키기 위해 규칙을 적용하여 문제가 없는지 확인!
 * DBA = Database Administrator
 * DB Developer

---

# MySQL

## 사용법
 포트 번호와 Password 꼭 기억할 것!!
 > * create database (원하는 DB 이름);
 > * create user '(원하는 DB 이름)'@'%' identified by '(원하는 DB 이름)';
 > * create user '(원하는 DB 이름)'@'localhost' identified by '(원하는 DB 이름)';
 > * grant all privileges on (원하는 DB 이름).* to '(원하는 DB 이름)'@'%';
 > * grant all privileges on (원하는 DB 이름).* to '(원하는 DB 이름)'@'localhost';
 > * flush privileges;
 > * use (생성한 DB);
