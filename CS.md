1. 브라우저 주소창에 www.google.com을 입력하면 어떤 일이 일어나나요?
2. DNS에 대해 설명해주세요.

-DNS (Domain Name System Servers) URL들의 이름과 IP주소를 저장하고 있는 데이터 베이스
숫자로 된 IP주소 (12.332.485.684) 대신 사용자가 사용하기 편리한 주소로 매핑해주는 역할

-TCP/IP 전송제어규약, 인터넷 규약
송수신자의 논리적 연결을 생성하고 IP 주소를 사용해서 데이터를 전달하는 것

-HTTP Hypertext Transfer Protocol
클라이언트와 서버가 서로 통신할 수 있게 하기 위한 언어를 정의하는 어플리케이션 규약

1-1. 웹브라우저는 캐싱된 DNS 기록들을 통해 해당 도메인 주소와 대응하는 IP주소를 확인
1-2. 웹브라우저가 HTTP를 사용하여 DNS에게 입력된 도메인 주소를 요청
1-3. DNS가 웹브라우저에게 찾는 사이트의 IP주소를 응답



3. GET과 POST의 차이는?

GET - 클라이언트에서 서버로 어떤 리소스로 부터 정보를 요청하기 위해 사용되는 메서드

POST - 클라이언트에서 서버로 리소스를 생성하거나 업데이트하기 위해 데이터를 보낼 때 사용 되는 메서드다. 예를들면 게시판에 게시글을 작성하는 작업 등을 할 때 사용


차이점
1. 사용목적 : GET은 서버의 리소스에서 데이터를 요청할 때, POST는 서버의 리소스를 새로 생성하거나 업데이트할 때 사용한다.

DB로 따지면 GET은 SELECT 에 가깝고, POST는 Create 에 가깝다고 보면 된다.


2. 요청에 body 유무 : GET 은 URL 파라미터에 요청하는 데이터를 담아 보내기 때문에 HTTP 메시지에 body가 없다. POST 는 body 에 데이터를 담아 보내기 때문에 당연히 HTTP 메시지에 body가 존재한다.


3. 멱등성 (idempotent) : GET 요청은 멱등이며, POST는 멱등이 아니다.
GET은 리소스를 조회한다는 점에서 여러 번 요청하더라도 응답이 똑같을 것 이다. 반대로 POST는 리소스를 새로 생성하거나 업데이트할 때 사용되기 때문에 멱등이 아니라고 볼 수 있다. (POST 요청이 발생하면 서버가 변경될 수 있다.)


4. REST API에 대해 설명
REST (REpresentational State Transfer) 기본

* REST의 요소

  * Method

    | Method | 의미   | Idempotent |
    | ------ | ------ | ---------- |
    | POST   | Create | No         |
    | GET    | Select | Yes        |
    | PUT    | Update | Yes        |
    | DELETE | Delete | Yes        |

    > Idempotent : 한 번 수행하냐, 여러 번 수행했을 때 결과가 같나?
    <br>

  * Resource

    * http://myweb/users와 같은 URI
    * 모든 것을 Resource (명사)로 표현하고, 세부 Resource에는 id를 붙임

    <br>

  * Message

    * 메시지 포맷이 존재

      : JSON, XML 과 같은 형태가 있음 (최근에는 JSON 을 씀)

      ```text
      HTTP POST, http://myweb/users/
      {
      	"users" : {
      		"name" : "terry"
      	}
      }
      ```

    <br>

* REST 특징

  * Uniform Interface

    * HTTP 표준만 맞는다면, 어떤 기술도 가능한 Interface 스타일

      예) REST API 정의를 HTTP + JSON로 하였다면, C, Java, Python, IOS 플랫폼 등 특정 언어나 기술에 종속 받지 않고, 모든 플랫폼에 사용이 가능한 Loosely Coupling 구조

    * 포함
      * Self-Descriptive Messages

        * API 메시지만 보고, API를 이해할 수 있는 구조 (Resource, Method를 이용해 무슨 행위를 하는지 직관적으로 이해할 수 있음)

      * HATEOAS(Hypermedia As The Engine Of Application State)

        * Application의 상태(State)는 Hyperlink를 통해 전이되어야 함.
        * 서버는 현재 이용 가능한 다른 작업에 대한 하이퍼링크를 포함하여 응답해야 함.

      * Resource Identification In Requests

      * Resource Manipulation Through Representations

  * Statelessness

    * 즉, HTTP Session과 같은 컨텍스트 저장소에 **<u>상태 정보 저장 안함</u>**
    * **<u>Request만 Message로 처리</u>**하면 되고, 컨텍스트 정보를 신경쓰지 않아도 되므로, **<u>구현이 단순해짐</u>**.

    * 따라서, REST API 실행중 실패가 발생한 경우, Transaction 복구를 위해 기존의 상태를 저장할 필요가 있다. (POST Method 제외)

  * Resource 지향 아키텍쳐 (ROA : Resource Oriented Architecture)

    * Resource 기반의 복수형 명사 형태의 정의를 권장.
  
  * Client-Server Architecture
  
  * Cache Ability
  
  * Layered System
  
  * Code On Demand(Optional)
5. 객체 지향 프로그래밍이란?

순차적,비구조적 프로그래밍 -> 객체지향 프로그래밍

특정한 개념의 함수와 자료형을 함께 묶어서 관리하기 위해 탄생한 것

객체 내부에 자료형(필드)와 함수(메소드)가 같이 존재하는 것

1. 추상화
    추상적인 개념에 의존하여 설계해야 유연함을 갖출 수 있다.

2. 캡슐화
    한 곳에서 변화가 일어나도 다른 곳에 미치는 영향을 최소화 시키는 것
    낮은 결합도(어떤 기능을 실행할 때 다른 클래스나 모듈에 얼마나 의존적인가)를 유지할 수 있도록 설계하는 것

3. 상속
    여러 개체들이 지닌 공통된 특성을 부각시켜 하나의 개념이나 법칙으로 성립하는 과정
    


6. 자료구조 stack과 queue에 대해 설명
https://github.com/gyoogle/tech-interview-for-developer/blob/master/Computer%20Science/Data%20Structure/Stack%20%26%20Queue.md
7. 프로세스와 스레드에 대해 설명
https://github.com/gyoogle/tech-interview-for-developer/blob/master/Computer%20Science/Operating%20System/Process%20vs%20Thread.md
