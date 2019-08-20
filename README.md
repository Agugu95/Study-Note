# 짬짬이 기록하는 기록기록기

1. Reverse DNS  
2. Sequlize / Migration / DB ORM => DB ORM을 위해 Sequlize 프레임워크를 사용  
3. Node-Exepress   
5. HeidiSQL과 터널링, 파이프라인 
6. MS ISS 와 톰캣

# 2019.08.19

일일 공부 계획은 JDBC / ODBC / ORM / WAS에 대하여 정리하는 것  

실제로 한 것
- ORM이란 무엇인가?  
ORM은 보통 JPA (Java Persistence API)를 뜻하며, Java EE의 표준 ORM 기술 방식이라고 한다.  
RDB의 테이블을 객체지향적으로 사용하기 위한 목적을 가지고 있는데  
여기서 의문은 "왜 RDB 테이블을 객체지향적으로 사용해야하는가?" 였다.  
**그 이유는 RDB 자체는 Relational Data Base로 테이블 자체는 Key : Value 방식으로 존재하고 이는 객체로써의 접근을 어렵게 만들기 때문에  
사용을 한다는데 이 부분은 조금 더 알아봐야할듯**  
결론적으로 ORM을 사용하는 이유는 SQL을 통한 테이블에 대한 접근을 최대한 줄여, 비지니스 로직에 집중하기 위함이고  
이로써 얻을 수 있는 장점은 SQL을 직접 작성하지 않아도 되며, CRUD에 대한 반복적인 작업을 대신해줄 수 있다는 것  
-> 이게 아마 HeidiSQL을 사용했을 때랑 비슷한 것 같은데, RDB의 테이블을 모델(객체)로 매핑해서 사용하는 것과 비슷한 것 같다.  
차이를 알아봐야겠다.  
자바에서는 Hibernate를 사용하는 듯 

- JDBC란 무엇인가?  
JDBC는 Java DataBase Connectivity로 자바에서 RDB에 직접 접근할 수 없으니, 그것을 대신 해주는 자바 내장 API다.  
RDB에 접근해서 역할을 수행하기때문에 Core API라고도 하고, RDB의 연결 과 Query 실행 및 트랜잭션 관리까지 지원해준다.  
근데 문제는 JDBC만으로는 실제로 역할을 수행할 수 없다는게 유머  
JDBC 드라이버가 필요한데, 실제로는 JDBC 드라이버가 자바 어플리케이션 상의 요청을 DBMS의 형태로 변경하여 전달해준다.  
>MySQL Connector와 같은 것들이 이에 해당하는듯  
당연히 DBMS가 하나만 존재하는 것이 아니니 내가 Oracle도 사용하고 싶고, MariaDB도 사용하고싶다면 전부 다른 JDBC 드라이버를 사용해야한다.  
그래서 이를 보완하기 위해서 존재하는 것이 ODBC와 추상화 라이브러리다.  
**0820 추가**  
실제로 JDBC의 경우에는 하나의 테이블을 조작한다고 했을 때 그 테이블을 조작하는 쿼리가 전부 소스코드 안에 들어가게 된다.  
>Mybatis와 JDBC는 뭐가 다른가? <https://hub.packtpub.com/why-mybatis/>  

- JDBC와는 다른 ODBC  
  
  > 이외에 0819 재정리한 것  
  Call by Value(Refrance), (멀티)프로세스/(멀티)스레드, 포인터와 배열, GC, JVM, DeadLock, Mutex와 Semaphore, Serialization, Sync/Async,  
  Blocking/Non-Blocking, OOP SOLID 원칙, Static/Non-Static, Over Loading/Riding, Interface/Abstract 
