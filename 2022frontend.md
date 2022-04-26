2022 Frontend Framework 소개 및 트렌드 공유

Framer

vue - 개인 프로젝트용으로 많이 사용
react - 기업 프로젝트로 대부분 사용
angular - si 또는 100명 이상의 개발팀인 곳에서 사용

web framework등장
- jquery 로 떡칠된 웹페이지
- DOM Tree 특유의 느린 update api 성능 + 브라우저 엔진으로 인해 스크립트
- 웹 개발자의 메인 빌런 IE 6,7가 현역

웹에서 과감한 ui update가 불가능

chrome v8 code - machine code로 최적화
SPA를 만드는데에 최적화된 프레임워크들이 생겨나기 시작 -> MSA가 대세가 되었음

React
Virtual DOM
화면이 변경되는 시점?
rendering을 최소화

awesome react -  중요 라이브러리

web comoonents?

모바일 앱 개발 - flutter
IOS android desktop web까지 개발 가능
ios, android specific한 기능도 사용 가능

flutter 앱 시작 시에 CICD - codemagic

웹앱은 성능을 높이기 위해 많은 노력이 필요하다
그러나 개발 효율성은 높다

무조건 typescript 쓰자!

nextjs with typescript


Global state management
1. Context api - 성능 이슈가 존재한다.(초보자들)
2. redux - 2022 부터는 쓰지 마세요!, dispatcher 를 이용해서 순서 정리. 그래도 쓰고 싶으면 redux-toolkit을 사용해라! , RTX query도 나옴. 규칙 체계가 필요할때, 순수함수이기 때문에 지연이 없다.
3. mobx - 
4. zustand - redux보다 훨씬 쉽다.
5. recoil
6. jotai

Store 기반 - 전역 클래스
Flux패턴이란?

Atom 기반 - 전역 변수


swr 또는 react query - api 결과값을 다 담당 가능
cookie, local

1. 로그인 정보
2. 회원가입
3. 뭔가 복잡한 create 페이지
4. 사용자 로그 임시 저장

Next.js - 
remix - 서버가 더 많이 사용하고, 사용자가 편리하다. 초보자에겐 추천 X
cra + vite - 빠르게 빌드된다. SEO는 못한다.

Next.js
SSG
ISR

Tailwind - 
Bootstrap - 
Emotion - 
styled-jsx - 


Jest+ React-testing-library


구글, 네카라쿠 등 큰 기업, 현업에 있는 멘토님들로 구성해서 기획보단 오버엔지니어링에 집착하세요
대용량 트래픽 대응, lighthouse 100 100 100 100 점 찍기, tdd를 통한 코드 품질 향상, spring등 을 활용한 복잡한 디자인 패턴 숙지, 
sql 쿼리 최적화 등 현업에서 생긴법한, 현업에서 중점적으로 사용하는 내용들, 채용공고에서 우대사항에 있던 바로 그ㅓㅅ들을 적극 트레이닝하세요
앱출시, 고객반응 보기 안해도 됩니다. 최종발표까지 demo를 만들기만 하세요. 대신 퀄리티 있게 만드는데에 집중하고 면접에서 잘 대답할 수 있을 정도로 기술적인 내용을 숙지하세요.
과정 긑나고 이 프로젝트를 어떻게할지 생각하지 말고 구현

Pain Killer를 생각해라


www.first1000.co
Disquiet.io

painpoint를 겪고 있는 타겟 유저와의 1:1 심층 인터뷰
1. 매년 모두에게 강조하지만 이것 빼고 다른것들만 다함
2. 설문 등은 큰 도움 안됨
3. 솔루션을 듣지 말고 문제점을 듣는데에 집중

analytics 필수
채널톡 등으로 의견 수집 준비

