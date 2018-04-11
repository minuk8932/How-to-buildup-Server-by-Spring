# ORM
객체 관계 매핑(Object-relational mapping; ORM)은 데이터베이스와 객체 지향 프로그래밍 언어 간의 호환되지 않는 데이터를 변환하는 프로그래밍 기법이다. 객체 관계 매핑 라고도 부른다. 객체 지향 언어에서 사용할 수 있는 "가상" 객체 데이터베이스를 구축하는 방법이다. 객체 관계 매핑을 가능하게 하는 상용 또는 무료 소프트웨어 패키지들이 있고, 경우에 따라서는 독자적으로 개발하기도한다. 프레임워크 종류에는 **Mybatis, Hibernate, iBatis, EclipseLink** 등이 있음. (출처 : wikipedia) <br>
의의 : 코드의 반복적이고 지루한 부분을, 줄일 수 있고 SQL에 의존적인 코딩에서 벗어나, 생산적인 코딩이 가능하고, 유지보수가 편리해짐.
<br><br>

# MVC Pattern
MVC Pattern은 스프링 프레임워크에서 자체적으로 지원되고 있다. Model, View, Controller를 의미하는 것으로 소프트웨어 디자인 패턴이다. MVC에서 모델은 애플리케이션의 정보(데이터)를 나타내며, 뷰는 텍스트, 체크박스 항목 등과 같은 사용자 인터페이스 요소를 나타내고, 컨트롤러는 데이터와 비즈니스 로직 사이의 상호동작을 관리한다. <br>
*항목별로 좀 더 자세히 알아보면,* <br>
> - Model : 데이터 저장소와 연동해 사용자가 입력한 데이터나 출력 할 데이터, 그리고 트랜잭션을 컨트롤한다. DAO, Service 클래스가 모델 구성요소에 해당한다.
> - View : 모델이 처리한 데이터나 작업 결과를 가지고 화면을 띄워준다. 화면은 웹브라우저가 출력하고, 뷰 컴포넌트는 HTML/CSS/JavaScript를 사용해 웹 브라우저가 출력 할 UI를 생성한다. 일반적으로 HTML과 JSP를 통해 작성한다.
> - Controller : 클라이언트의 요청을 실제 업무를 수행하는 모델 구성요소를 호출한다. 모델 호출 시 전달하기 쉽게 데이터를 가공해주고, 모델의 수행 결과를 통해 화면을 생성하도록 뷰에 전달한다. 일반적으로 Servlet JSP를 이용해 작성한다.
- **모델**에 데이터에 대한 정의를 하고, 이를 실제로 보여주는것이 **뷰**, 그리고 데이터들을 처리하는 방식 또는 기능 등이 **컨트롤러**에 해당한다.

<img src="https://github.com/minuk8932/What-is-JPA/blob/master/img/mvc-pattern.png" width=200>

[그림 1] MVC Pattern
<br><br>

# Spring Framework
자바 플랫폼을 위한 오픈소스 애플리케이션 프레임워크로서 간단히 스프링(Spring)이라고도 불린다.
동적인 웹사이트를 개발하기 위한 여러가지 서비스를 제공하고 있다.
대한민국 공공기관의 웹 서비스 개발 시 사용을 권장하고 있는 전자 종부 표준프레임워크의 기반 기술로서 쓰이고 있다.
ORM 프레임워크와의 연결고리를 제공한다.
<br><br>

# Spring Triangle
> - POJO : Plain Old Java Object / 오래된 방식의 자바 객체를 의미하는 말인데, 스프링에서는 구현을 위해 특정한 인터페이스를 구현하거나 상속을 받을 필요가 없어 기존에 존재하는 라이브러리 등을 지원하기에 용이하고 객체가 가벼운 것이 특징이다.
> - PSA : Portable Service Abstraction / 트랜잭션 추상화, OXM 추상화 , 데이터 액세스의 Exception 변환기능 등 기술적인 복잡함은 추상화를 통해 Low Level의 기술 구현 부분과 기술을 사용하는 인터페이스로 분리한다. 즉, 인터페이스와 구현부의 분리를 말한다.
> - AOP : Aspect Oriented Programming / 공통로직을 별도의 공간에 따로 구현하고, 이를 런타임(실행시간)에 적용이 필요한 클래스 메소드에 프록시를 사용해 적용하는 기술을 말한다. 기존의 관점 지향 프로그래밍 프레임 워크인 AspectJ 또한 내부에서 사용가능하다. OOP를 좀 더 효율적으로 만들어 나가기위한 도구.
> - IoC/DI : Inversion of Control/Dependency Injection / 제어의 역전과 의존성 주입이라 번역이되는데, 이는 해당 컨테이너가 객체의 생성 및 관계설정, 의존성 주입을 통해 개발자가 직접하지 않고 프레임워크가 대신 맡아서 처리하는것을 말한다.

<img src="https://github.com/minuk8932/What-is-ORM/blob/master/img/spring-triangle.png" width=200>

[그림 2] Spring Triangle
<br><br>

# JPA
Java Persistence API의 약자로, 자바 진영의 ORM 기술 표준이다. JPA는 application과 JDBC 사이에서 동작한다. JPA는 EJB(Enterprise Java Beans) 3.0에서 하이버네이트 기반으로 만들어진 ORM 기술에 대한 API 표준 명세다.(즉, 인터페이스들의 집합)
<br><br>

# Why JPA?
1. 생산성 : JPA를 사용하면 자바 컬렉션에 객체를 저장하듯이 JPA에게 해당 객체를 전달하면 된다. SQL 명령어나, JDBC API를 사용하는 반복적인 일은 JPA가 대신 처리해준다. <br>
```Java
// 예제 코드 : 객체를 컬렉션에 저장하듯이 JPA에게 전달하는 코드

jpa.persist(member); // 저장
Member member = jpa.find(memeberId); // 조회
```
<br>

2. 유지 보수 : JPA의 기능으로 코드가 간략해져, 유지보수에 걸리는 시간이 줄어들었다.
- 좀 더 자세히 말하면, JDBC 사용시 엔티티에 필드 하나만 추가되어도, 관련된 등록/수정/조회 SQL과 결과를 매핑하기위한 모든 코드를 변경해야 했지만, JPA를 사용하면 이러한 과정을 JPA가 대신 처리해 주기 때문에, 수정해야 할 코드길이가 줄어든다.
<br>

3. 패러다임의 불일치 해결 : JPA는 상속, 연관관계, 객체 그래프 탐색, 비교하기와 같은 **_패러다임의 불일치_** 문제를 해결해준다.
- 객체 지향 언어와 그에 따라 데이터베이스에 데이터를 저장하는데 생기는 문제들로, 예를 들어 어떤 팀 객체를 참조하고있는 회원 객체를 저장하려 할 때는 해당 팀 객체도 함께 저장하지 않으면 참조하는 팀 객체를 잃는 문제가 발생한다. 즉 간단히 말하면, 객체 구조를 테이블 구조에 저장하는데 있어 발생하는 한계에 따른 문제를 **_패러다임의 불일치_** 라고한다.
<br>

4. 성능 : 객체 재사용을 통해 성능이 좋아지고, 지속적인 DB로의 접근을 막는다. <br>
```Java
// 예를 들어 이러한 코드 같은 경우, 데이터베이스와의 반복적인 통신이 필요하다.
String memberId = "memberId1";
Member member1 = jpa.find(memberId);  // JPA가 아닌경우 DB 1회 접근
Member member2 = jpa.find(memberId);  // DB 2회 접근
```
- 그러나, JPA를 어플리케이션과 데이터베이스 사이에 두면, 조회하는 SQL문을 1회만 데이터베이스로 전달하고, 그 다음부턴 조회한 회원 객체 재사용이 가능해 성능을 높힐 수 있다.
<br>

5. 데이터 접근 추상화와 벤더 독립성 : JPA는 어플리케이션과 데이터베이스 사이에 추상화된 데이터 접근 계층을 제공하여, 특정 데이터베이스 기술에 종속되는 것을 피한다. 이 계층을 **Dialect(방언)** 이라고 하는데, 만약 데이터베이스를 변경하게 되면, 다른 데이터베이스를 사용한다고 선언해주기만 하면 된다.
<br>

6. 표준 : JPA는 표준 기술으로서, 다른 구현 기술로 손쉽게 변경이 가능하다.
<br><br>

# Persistence Context
'엔티티를 저장하고 관리'하는 것이 영속성 컨텍스트인데, 이 컨텍스트는 내부의 1차캐시를 갖고, 해당 캐시내에 영속성 상태의 엔티티를 저장해둔다.
JDBC와 DB사이에서 작동하며, 반복적인 DB로의 접근을 막고 영속성 상태의 엔티티를 반환해 주는 역할을 한다.<br>
아래와 같은 방식으로 영속성 컨텍스트가 동작하며 DB로의 접근을 줄여준다.<br>
```
1. 조회할 데이터가 영속성 컨텍스트에 존재하는지 확인
2. 데이터가 없으면 쿼리를 생성
3. 쿼리를 DB에 전송
4. 결과 값을 영속성컨텍스트가 전달 받음
5. 전달 받은 데이터를 엔티티로 저장
6. 엔티티 인스턴스를 리턴
```

해당 내용은 공부하며 지속적으로 수정해나갈 계획입니다.
