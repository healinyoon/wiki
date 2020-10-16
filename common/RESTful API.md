# RESTful API

## RESTful API?

`REST` 의 기본 원칙을 성실히 지킨 API

## REST

`REST` 는 REpresentational State Transfer의 약자이다. 

WWW와 같은 분산 하이퍼미디어 시스템을 위한 소프트웨어 아키텍처의 형식으로, "웹에 존재하는 모든 자원(이미지, 동영상, DB 등등)에 고유한 URI를 부여하여 활용"하는 것으로 자원을 정의하고, 자원에 대한 주소를 지정하는 방법론을 의미한다.

## REST의 기본 원칙

> REST의 기본 원칙은 무엇인가?

REST의 6가지 원칙

- 인터체이스 일관성(Uniform Interface)

    : URI로 지정한 자원에 대한 조작을 통일되고 한정적인 인터페이스로 수행한다. HTTP 표준에만 따른다면 모든 플랫폼에서 사용이 가능하다.

- 무상태(Stateless)

    : HTTP는 Stateless 프로토콜이므로 REST 역시 무상태성을 가진다 ⇒ 작업을 위한 상태 정보를 저장/관리하지 않는다.

    예) 세션, 쿠키 정보를 별도로 저장/관리하지 않아서 API 서버는 들어오는 요청만 처리하면 된다.

- 캐싱 가능(Cachealble)

    : 웹 표준 HTTP 프로토콜을 그대로 사용하므로, 웹에서 사용하는 기존의 인프라를 그대로 활용 가능하다 ⇒ HTTP의 캐싱 기능 사용 가능하다.

- 클라이언트-서버 구조(Client-Server)

    : 자원을 요청하는 Client, 자원이 있는 Server 구조를 가진다.

- 계층화(Hierarchical system)

    : API 서버는 순수 비즈니스 로직을 수행하고 그 앞단에 사용자 인증, 암호화, 로드 밸런싱 등을 수행하는 계층을 추가하여 구조상의 유연성을 줄 수 있다.

- 자체 표현 구조(Self-descriptiveness)

    : REST API 메세지만 보고도 이해할 수 있도록 자체 표현 구조로 되어있다.

## REST의 구성요소

> REST는 어떻게 구성하는가?

### 자원(Resource), URI

서버에 존재하는 모든 자원은 고유한 ID를 가지며, 클라이언트는 ID를 통해  서버에 자원 요청을 보낸다. 

예) `/user/{userId}`

### 행위(Verb), Method

클라이언트의 요청을 표현하는 방법으로, HTTP 프로토콜에서는 `GET`,  `POST`, `PUT`, `DELETE` Method를 제공한다.

### 표현(Representations)

클라이언트와 서버가 데이터를 주고받는 형식으로 json, xml, text, rss 등이 있다.

## RESTful한 API 요약

> 마지막으로 RESTful한 API를 만들기 위한 내용!

1. 리소스와 행위를 명시적이로 직관적으로 분리한다.
    - 리소스 = URI ⇒ 명사로 표현
    - 행위 = Method ⇒ GET, POST, PUT, DELETE
2. 메세지는 Header와 Body를 명확하게 분리한다.
    - 애플리케이션 서버가 행동할 판단의 근거가 되는 컨트롤 정보인 API 버전 정보, 응담받고자 하는 MIME 타입 등은 Header에 담는다.
    - Entity에 대한 내용은 Body에 담는다.
3. API 버전을 관리한다.
    - 특정 API를 변경할 때는 반드시 하위 호환성을 보장한다.
4. 서버와 클라이언트가 같은 방식을 사용하여 요청하도록 한다.
    - 즉 URI가 플랫폼 중립적이여야 한다.

> (참고) URL vs URI
URL은 Uniform Resource Locator로 인터넷 상 자원의 위치를 의미합니다. 자원의 위치라는 것은 결국 어떤 파일의 위치를 의미합니다. 반면에 URI는 Uniform Resource Identifier로 인터넷 상의 자원을 식별하기 위한 문자열의 구성으로, URI는 URL을 포함하게 됩니다. 그러므로 URI가 보다 포괄적인 범위라고 할 수 있습니다.

## 참고

[[개발 상식] RESTful API](https://mizzo-dev.tistory.com/entry/RESTfulAPI)

[REST란](https://medium.com/@hckcksrl/rest%EB%9E%80-c602c3324196)

[[Server] Restful API란?](https://mangkyu.tistory.com/46)