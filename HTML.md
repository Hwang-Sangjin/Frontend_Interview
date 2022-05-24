HTML5는 W3C에서 2014년에 공식 표준화

2019년에 WHATWG(애플, 모질라, 구글, MS)에 의해 HTML Living Standard가 표준화

웹표준을 준수하여 작성하여아한다.

웹사이트 제작시 고려 사항

1. 웹 표준 - 웹 사이트를 작성할 때 따라야 하는 공식 표준이나 기술 규격
2. 웹 접근성 - 장애의 여부와 상관 없이 모두가 웹사이트를 이용할 수 있게 하는 방식
3. 크로스 브라우징 - 모든 브라우저 또는 기기에서 사이트가 제대로 작동하도록 하는 기법

<!--  -->

Tag

Element

1. Opening tag - <요소의 이름>
2. Closing tag - </요소의 이름>
3. Content - 요소의 내용
4. Element - 여는 태그, 닫는 태그, 내용

태그는 대소문자를 구분하지 않지만, HTML5에서는 모두 소문자로 작성을 권장

Empty Element
내용이 없는 Element
이 경우 닫는 태그를 추가로 명시하지 않아도 된다.
HTML5에서는 <br>, <br/> 은 같다. 예전 문법은 꼭 추가해야함
ex)image, 수평선, 줄바꿈, input, meta

요소의 중첩(Nesting)

1.  요소 안에 다른 요소가 들어가는 포함 관계를 성립할 수 있다.
2.  이렇게 여러 요소가 중첩될 경우에는, 열린 순서의 반대로 닫혀야만 한다.
3.  이렇게 서로의 포함 관계를 구분하기 위하여 들여쓰기를 사용한다.

<ul>
    <li>하나</li>
    <li>둘</li>
    <li>셋</li>
</ul>

<!--  -->

Comments

브라우저는 주석을 무시하며 사용자가 주석을 보이지 않게 한다.

주석의 목적은 코드에 메모를 추가하거나, 혹은 사용하지 않는 코드를 임시로 처리하기 위함이다.

HTML 문서의 구조

<!DOCTYPE html>

html - 페이지 전체의 컨텐츠를 감싸는 root 요소
head - 웹 브라우저 화면에 직접 나타나지 않는 웹페이지의 정보
meta tag - 문서의 일반적인 정보와 문자 인코딩을 명시, SEO
title - 웹 타이틀

Head태그
head 요소는 기계가 식별할 수 있는 문서 정보(meta 데이터)를 답습니다.
정보로는 문서가 사용할 title, script, stylesheet 등이 있습니다.

하나 이상의 meta 데이터 콘텐츠
단 한개의 title 요소를 포함

MDN 참고

Body 태그
body 요소는 HTML 문서의 내용을 나타냅니다. 한문서에 하나의 body 요소만 존재

Tag를 구분 짓는 특성 (body)

1. 구획을 나누는 태그
2. 그 자체로 요소인 태그

3. Block - 언제나 새로운 줄에서 시작하고, 좌우 양쪽으로 최대한 늘어나 가능한 모든 너비를 차지합니다.
4. Inline - 줄의 어느 곳에서나 시작할 수 있습니다
   바로 이전 요소가 끝나는 지점부터 시작하여, 요소의 내용만큼만 차지합니다.

포함 규칙
블록> 블록
인라인> 인라인
블록은 인라인 요소를 포함할 수 있다.
인라인은 블록 요소를 포함할 수 없다.

콘텐츠 카테고리

1. Metadata Content - 문서의 메타 데이터, 다른 문서를 가르키는 링크 등을 나타내는 요소
2. Flow Content - 웹 페이지상에 메타데이터를 제외하고 거의 모든 요소, 보통 텍스트나 임베디드 콘텐츠를 포함
3. Section Content - 웹 문서의 Section을 나눌 때 사용
4. Heading Content - section의 heading과 관련된 요소
5. Phrasing Content - 문단에서 텍스트를 마크업 할 때 사용
6. Embedded Content - 이미지나 비디오 등 외부 소스를 가져오거나 삽입할 때 사용되는 요소
7. Interactive Content - 사용자와의 상호작용을 위한 컨텐츠 요소

Heading

<h1>
<h2>
<h3>
<h4>
<h5>
<h6>
- user Agent(웹 브라우저)가 제목 정보를 사용해 자동으로 문서 콘텐츠의 표를 만듬 - 순서를 지켜서 heading을 사용
- 글씨 크기를 위해 제목 태그를 사용하지 마라
- 페이지 하나 다 h1 하나만 사용 - SEO에 더 적합

Paragraph

<p>
- 콘텐츠를 문단으로 나누면 페이지의 접근성을 높인다.
- 스크린 리더 등 보조 기술은 다음 문단으로 넘어갈 수 있는 단축키를 제공함
- 빈 <p> 요소를 사용해 문단 사이에 여백을 추가하지 말것

Break

<br>
- html에서는 빈 공백을 다중으로 작성하여도 하나로 표시된다.
- 그래서 줄 바꿈을 위해서 <br>을 사용한다.
- 여러개의 <br>을 중첩해서 사용하기 보단 css를 이용한다.

<blockquote>
<q>

- 둘 다 인용을 다루는 요소
- blockquote는 block 요소
- q는 인라인 요소, ""로 구성해준다.

Preformatted

<pre>
- HTML에 작성한 내용 그대로 표현
- 고정폭 글꼴을 사용해 렌더링 한다.

Figure

<figure>
- 독립적인 콘텐츠를 표현
- figcaption 요소를 이용하여 같이 사용

Horizon Rule

<hr>
- 가로줄로 표현
- css를 추가하여 디자인 수정

Abbraviation

<abbr>
- title 속성을 이용하여 약어 표현

Address

<address>
- 주소라는 의미를 탐는 태그

Cite

<cite>
- 인용의 출처를 표시해주는 태그

Bidirectional override

<bdo>
- dir= "rtl", dir="ltr"로 오른쪽에서 왼쪽으로 표시, 왼쪽에서 오른쪽으로 표시 가능




Forammating

Bold
<b>
- 굵은 글씨 요소
- 요약의 키워드
- 특별히 중요하지 않지만 굵게 표시하고 싶은 요소

Strong
<strong>
- 굵은 글씨 요소
- 높은 중요도 요소

Italic
<i>
- 기울임꼴로 표시
- 기술용어, 외국어 구절, 등장인물의 생각

Emphasize
<em>
- 기울임 꼴로 표시
- 텍스트의 강세를 나타냄

Mark
<mark>
- 중요한 표시, 하이라이트한 부분

Small
<small>
- 덧붙이는 글이나, 저작권과 법률 표기등
- 작은 텍스트로 표시

Supper
<sup>
- 윗 첨자 표시
- 지수 표시할 때

Sub
<sub>
- 아래 첨자 표시
- 화학식에 표시, 각주 표시

Delete
<del>
- 문서에서 제거된 텍스트의 범위

Insert
<ins>
- 문서에서 추가된 템스트의 범위

Code
<code>
- 인라인 요소
- 여러줄의 코드를 나타내려면 <pre>로 감싸서 <code>를 사용해라
- 짧은 코드 조각을 타냄

Kdb
<kdb>
- 키보드 입력 요소를 나타냄





Anchor
<a>
- 하이퍼 링크를 만드는 태그
- 절대경로, 상대경로를 이용하여 이동 가능하다
- 이메일, 전화
- 속성1: href, 속성2: target

target
- _self - 현재 브라우징에 표시, default 값
- _blank - 새로운 브라우징에 표시
- _parent - 현재 브라우징 맥락의 부모에 표시, 없으면 _self와 동일
- _top - 최상단 브라우징 맥락에 표시, 없으면 _self와 동일


Entity
- HTML에서 문자 <, >, ", &는 특수 문자입니다. 따라서 이를 표현해주기 위하여 Entity로 표현
< - &lt;
> - &gt;
" - &quot;
' - &apos;
& - &amp;
(     ) - &nbsp;



구조를 나타내는 요소

Semantic 웹
- 의미론적인 마크업을 사용하여 만든 웹

Semantic 웹의 장점
- SEO
- 스크린리더로 페이지를 탐색할 때
- 웹 접근성이 높다
- 개발자간의 협업 시에 유리하다

Div
<div>
- block 컨테이너
- 순수 컨테이너로서 아무것도 표현하지 않는다.

Span
<span>
- inline 컨테이너
- 순수 컨테이너로서 아무것도 표현하지 않는다.

Header
<header>
- 소개, 탐색에 도움을 주는 컨텐츠
- 제목, 로고, 검색폼, 작성자 이름
- 하나만 사용해야함

Footer
<footer>
- 작성자, 저작권 정보, 관련 문서의 컨텐츠
- 하나만 사용해야함

Navigation
<nav>
- 현재 페이지 내, 또는 다른 페이지로의 링크를 보여주는 구획
- 메뉴, 목차, 색인

Aside
<aside>
- 주요 내용과 간접적으로 연관된 부분
- 주로 사이드바 혹은 콜아웃 박스로 표현

Main
<main>
- body 태그의 하위로 사용되며, 딱 한번 사용된다.
- internet explorer에서는 지원하지 않아서 <main role="main">으로 작성

Article
<article>
- 독립적으로 구분해 배포하거나 재사용할 수 있는 구획
- 게시판과 블로그 글, 매거진이나 뉴스기사 에서 사용

Section
<section>
- 일반 구획 요소
