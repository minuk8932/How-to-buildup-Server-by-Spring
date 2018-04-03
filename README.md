# What-is-ORM
객체 관계 매핑(Object-relational mapping; ORM)은 데이터베이스와 객체 지향 프로그래밍 언어 간의 호환되지 않는 데이터를 변환하는 프로그래밍 기법이다. 객체 관계 매핑 라고도 부른다. 객체 지향 언어에서 사용할 수 있는 "가상" 객체 데이터베이스를 구축하는 방법이다. 객체 관계 매핑을 가능하게 하는 상용 또는 무료 소프트웨어 패키지들이 있고, 경우에 따라서는 독자적으로 개발하기도한다. 종류에는 Mybatis, Hibernate, JPA 등이 있음. (출처 : wikipedia)
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
> - AOP : Aspect Oriented Programming / 공통로직을 별도의 공간에 따로 구현하고, 이를 런타임(실행시간)에 적용이 필요한 클래스 메소드에 프록시를 사용해 적용하는 기술을 말한다. 기존의 관점 지향 프로그래밍 프레임 워크인 AspectJ 또한 내부에서 사용가능하다.
> - IoC/DI : Inversion of Control/Dependency Injection / 제어의 역전과 의존성 주입이라 번역이되는데, 이는 해당 컨테이너가 객체의 생성 및 관계설정, 의존성 주입을 통해 개발자가 직접하지 않고 프레임워크가 대신 맡아서 처리하는것을 말한다.

[그림 1] Spring Triangle
<img src="https://github.com/minuk8932/What-is-ORM/blob/master/img/spring-triangle.png" width=200>
