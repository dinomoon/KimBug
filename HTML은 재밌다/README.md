# HTML은 재밌다.

**HTML이 중요한 이유?**

- 웹페이지의 가장 기본이다.
- 문서의 구조와 정보 위계가 명확하게 보이는 아름다운 HTML 코드를 작성하자. -> Semantic Markup -> 검색 엔진 최적화에 도움이 된다.(Search Engine Optimization)

---

**태그 해부학**

- p태그 안의 문단이 `러시아어`라면 `lang="ru"`라는 attribute와 value를 줄 수 있다.

**Heading과 Paragraph**

- h1~h6태그
- p태그

**강조 Emphasis**

- em태그 또는 strong태그
  > 디테일한 부분은 css로 꾸미면 된다. 중요한 건 브라우저에게 이 부분이 중요하다는 정보를 준다는 것이다.

**링크 Anchor**

- href속성의 값으로 가능한 것들
  - 웹 URL
  - 페이지 내 이동
  - 메일주소
  - 전화번호
- target = "\_blank"

```html
<a href="https:www.naver.com"></a>
<a href="#section2"></a>
<!-- <section id='section2'></section>-->
<a href="mailto:ansrud1003@naver.com"></a>
<a href="tel:01012345678"></a>
```

**이미지 Image**

- 이미지 태그는 src와 alt 두개의 속성을 모두 적어줘야한다.

```html
<img src="절대경로" alt="고양이와 강아지" />
<img src="www.naver.com/cat" alt="고양이와 강아지" />

<img src="상대경로" alt="고양이" />
<img src="./images/cat.jpg" alt="고양이" />
```

**리스트 Lists**

- li안에는 뭐가 오든 상관없지만 ol, ul의 직계자식은 무조건 li만 올 수 있다!

**정의 리스트 Description List**

- dl(description list), dt(description term), dd(description data)
- dl의 직계 자식으로는 div, dt, dd만 올 수 있다.
- 추가로, definition의 줄임말인 dfn이라는 태그도 있다.
  > HTML 문서에서 해당 용어가 가장 처음 사용될 때 흔히 dfn태그를 사용하여 용어를 정의하게 됩니다.

```html
<!-- 올바른 예시 -->
<dl>
  <dt>
    <dfn>김버그</dfn>
  </dt>
  <dd>직업: 프론트엔드 개발자</dd>
</dl>

<dl>
  <dt>김버그</dt>
  <dt>Kimbug</dt>
  <dd>직업: 프론트엔드 개발자</dd>
</dl>

<dl>
  <div>
    <dt>김버그</dt>
    <dt>Kimbug</dt>
    <dd>직업: 프론트엔드 개발자</dd>
  </div>
  <div>
    <dt>데벨업</dt>
    <dt>DevelUp</dt>
    <dd>직업: 프론트엔드 개발자</dd>
  </div>
</dl>

<!-- 틀린 예시 -->
<dl>
  <section>
    <dt>김버그</dt>
    <dt>Kimbug</dt>
    <dd>직업: 프론트엔드 개발자</dd>
  </section>
  <section>
    <dt>데벨업</dt>
    <dt>DevelUp</dt>
    <dd>직업: 프론트엔드 개발자</dd>
  </section>
</dl>

<dt>김버그</dt>

<!-- dfn예시 -->
<p>
  A <dfn id="def-validator">validator</dfn> is a program that checks for syntax
  errors in code or documents.
</p>
```

**인용 Quotations**

- blockquote태그와 q태그가 존재한다.
- blockquote태그는 하나의 문단 자체나 문장이 인용되었을 때, q태그는 문단 안에서 어떤 문장이 인용되었을 때 사용한다.
  - blockquote의 cite속성은 인용한 사이트의 url, cite태그는 저자 또는 책 제목을 쓸 때 사용한다.
  - q태그는 큰따옴표를 자동으로 생성해준다.

```html
<blockquote cite="www.naver.com">
  우리가 겪을 수 있는 가장 아름다운 체험은 신비다.<br />
  신비는 모든 참 예술과 과학의 근원이다.
  <cite>- 알버트 아인슈타인</cite>
</blockquote>

<blockquote cite="https://bit.ly/2mvSYrT">
  <p>
    The study is the first to project the long-term outlook for Antarctica's
    largest penguins, which can grow 1.2 meters (four ft) tall, seeking to fill
    a gap in understanding climate change and wildlife in one of the remotest
    parts of the planet.
  </p>
  <p>
    Overall, numbers were set to fall by at least 19 percent from current levels
    by 2100 as sea ice melts. And two-thirds of colonies of the birds, which
    have distinctive golden head patches, would decline by more than half, it
    said.
  </p>
  <p>
    <q>It's not happy news for the emperor penguin,</q> said Hal Castellan of
    the U.S. Woods Hole Oceanographic Institution, a co-author of the study in
    the journal Nature Climate Change.
  </p>
  <cite>
    “Emperor Penguin Population to Slide Due to Climate Change”, Scientific
    American, June 29, 2014, https://bit.ly/2mvSYrT
  </cite>
</blockquote>
```

**흑마법 Div & Span**

- 아무런 의미를 가지고 있지 않다. 오로지 스타일링을 위한 태그이다.
  > 정말 아무리 생각해도 떠오르는 태그가 없을 때 사용...
