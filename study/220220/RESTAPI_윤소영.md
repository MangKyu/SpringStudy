# REST API

Representational State Transfer API

- HTTP 통신에서 어떤 자원에 대한 CRUD 요청을 Resource와 Method로 표현하여 특정한 형태로 전달하는 방식
- 쉽게말해 소프트웨어가 다른 소프트웨어로부터 지정된 형식으로 요청/명령을 받을 수 있는 수단
- HTTP을 사용하는 모범사례



## REST의 구성

- 자원(RESOURCE) - URI

  예를들어 학생 정보가 자원일 때, ‘students’를 자원의 표현으로 정한다. 

- 행위(Verb) - HTTP METHOD

- 표현(Representations)

  클라이언트와 서버가 데이터를 주고받는 형태로 JSON을 주로 사용한다.



## HTTP METHOD

![image-20220219233808734](../AppData/Roaming/Typora/typora-user-images/image-20220219233808734.png)



## REST의 특징

- Server-Client(서버-클라이언트 구조)

  서버-클라이언트 구조를 통해 서로 간의 의존성을 줄입니다. 서버는 API를 제공, 클라이언트는 사용자인증, 세션, 로그인 정보를 관리합니다.

- Stateless(무상태)

  스테이트리스(stateless) 요청 간에 클라이언트 정보가 저장되지 않으며, 각 요청이 분리되어 있고 서로 연결되어 있지 않는다.

  http 에서 주로 쓰는 방식, 문서 전달이 목적, 요청때만 연결된다. 그래서 로그인/회원가입때 문제가 생김, 이를 위해 시큐리티가 존재

  

  이와 반대되는 개념이 Stateful 

  Stateful -> 서버와 클라이언트끼리 채팅 가능, 데이터를 응답해줄 준비가 되어 있는 상태

  

- Cacheable(캐시 처리 가능)

  캐시(데이터를 임시로 저장해두는 장소)를 통해 대량의 요청을 효율적으로 처리할 수 있다.

- Layered System(계층화)

  Rest API의 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 등을 위한 계층을 추가하여 구조를 변경할 수 있습니다. 또한 Proxy, Gateway와 같은 네트워크 기반의 중간매체를 사용할 수있다.

- Uniform Interface(인터페이스 일관성)

  인터페이스의 특징인 낮은 결합도 형태를 떠올리면된다. HTTP를 사용하는 모든 플랫폼에서 요청이 가능하게 되었다는 뜻입니다. (모바일, 웹 다 가능)



## 예시

![image-20220219233943507](../AppData/Roaming/Typora/typora-user-images/image-20220219233943507.png)

컬렉션 : 여러개의 토픽을 표현 -> 복수명사 사용 (이것을 컬렉션이라 한다)

엘리먼트: 컬렉션이 모여있는 것



## REST 규칙

![image-20220219234039525](../AppData/Roaming/Typora/typora-user-images/image-20220219234039525.png)

1. URI는 명사를 사용한다.

2. 슬래시로 계층 관계를 표현한다.

3. URI의 마지막에는 슬래시를 붙이지 않는다.

4. URI는 소문자로만 구성한다.

5. 가독성이 떨어지는 경우 하이픈을 사용한다.

6. 파일 확장자는 포함하지 않는다.