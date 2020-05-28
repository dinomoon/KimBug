# HTML은 재밌다.

**HTML이 중요한 이유?**

- 웹페이지의 가장 기본이다.
- 문서의 구조와 정보 위계가 명확하게 보이는 아름다운 HTML 코드를 작성하자. -> Semantic Markup -> 검색 엔진 최적화에 도움이 된다.(Search Engine Optimization)
- Hyper Text Markup Language
  - Hyper Text는 다른 웹페이지로 넘어갈 수 있게 해주는 text이고, 웹페이지들은 하이퍼텍스트를 통해서 서로 연결되어있다.
  - Markup은 형광펜을 칠한 것과 같이 구분을 한다는 것인데, 태그를 이용해 문서의 어느 부분이 제목인지, 문단인지 역할을 구분을 해주는 것이다.
  - 우리가 개발할 때 편할 수도 있지만, 시각장애인 분들이나, 검색엔진을 위해 마크 업을 명확하게 해야한다.

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
- alt속성은 alternate의 줄임말로, 어떠한 이유로 이미지를 불러오지 못했을 때 이미지 대신 보여주는 대체 텍스트이다. 또한 시각장애인분들이 스크린 리더기를 사용하실 때, 스크린 리더기에서는 이미지를 alt의 내용을 읽어준다고 한다.

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

**Form**

- 반드시 써야하는 속성 2가지 -> action과 method
  - action은 form을 처리할 곳으로 보내는 주소를 적고 method는 처리할 방식을 적는다.(GET또는 POST)
- input

  ```html
  <form action="" method="GET">
    <input
      type="text"
      placeholder="아이디를 입력하세요"
      minlength="5"
      maxlength="13"
      required
    />
    <input
      type="text"
      placeholder="이름을 입력하세요"
      minlength="5"
      maxlength="13"
      value="최문경"
      disabled
    />
    <input type="email" placeholder="이메일을 입력하세요" />
    <input
      type="password"
      placeholder="비밀번호를 입력하세요"
      minlength="6"
      maxlength="14"
    />
    <input type="url" placeholder="포트폴리오 url을 입력하세요" />
    <input
      type="number"
      placeholder="10~20사이의 수를 적으세요"
      min="10"
      max="20"
    />
    <input type="file" accept=".jpg, .png" />
  </form>
  ```

- label

  ```html
  <form action="" method="GET">
    <label for="user-id" />
    <input type="text" required placeholder="아이디" />
  </form>
  ```

- radio & checkbox

  ```html
  <!-- name은 radio그룹을 만들어주는 속성이고 value는 어떤 radio가 선택되었는지 알려주는 값 -->
  <form action="" method="GET">
    <input type="radio" id="subscribed" name="subscription" value="1" />
    <label for="subscribed">구독</label>
    <input type="radio" id="unsubscribed" name="subscription" value="0" />
    <label for="unsubscribed">미구독</label>
    <button type="submit">submit</button>
  </form>

  <form action="" method="GET">
    <input type="checkbox" id="html" name="skills" value="html" />
    <label for="html">HTML</label>
    <input type="checkbox" id="css" name="skills" value="css" />
    <label for="css">CSS</label>
    <input type="checkbox" id="js" name="skills" value="js" />
    <label for="js">JS</label>
    <button type="submit">submit</button>
  </form>

  <!-- 제출 url: www.naver.com/?skills=html&skills=css&skills=js -->
  ```

- select & option

  ```html
  <form action="" method="GET">
    <label for="skill">skill</label>
    <select id="skill" name="skill">
      <option value="html">html</option>
      <option value="css">css</option>
      <option value="js">js</option>
    </select>
    <button type="submit">submit</button>
  </form>
  ```

- textarea

  ```html
  <form action="" method="GET">
    <label for="field">자기소개</label>
    <textarea id="field" placeholder="자기소개를 입력하세요" rows="" cols""></textarea>
  </form>
  <!-- rows와 cols는 보통 css로 작업해준다. -->
  ```

- button

  ```html
  <form action="" method="GET">
    <button type="button">버튼</button>
    <button type="submit">제출하기</button>
    <button type="reset">다시쓰기</button>
  </form>
  ```

- table

  ```html
  <table>
    <thead>
      <tr>
        <th scope="col">월</th>
        <th scope="col">화</th>
        <th scope="col">수</th>
        <th scope="col">목</th>
        <th scope="col">금</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th scope="row">1교시</th>
        <td rowspan="2">정보처리알고리즘</td>
        <td>데이터베이스개론</td>
        <td>통일과 남북한 관계의 이해</td>
      </tr>
      <tr>
        <th scope="row">2교시</th>
        <!-- <td rowspan="2">정보처리알고리즘</td> -->
        <td>웹프로그래밍2</td>
        <td>응용소프트웨어설계</td>
      </tr>
      <tr>
        <th scope="row" colspan="5">점심시간</th>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
      </tr>
    </tfoot>
  </table>
  ```

- 미디어 파일 Media

  ```html
  <!-- audio -->
  <audio src="" loop autoplay controls>
    <audio>
      <source src="" type="" />
      <source src="" type="" />
      <source src="" type="" />
      <p>브라우저를 업데이트하거나 크롬으로 바꾸세요..</p>
      <a href="https://browsehappy.com/">업데이트하러 가기</a>
    </audio>

    <!-- video -->
    <video src="" loop autoplay controls>
      <video autoplay>
        <source src="" type="" />
        <source src="" type="" />
        <source src="" type="" />
        <p>브라우저를 업데이트하거나 크롬으로 바꾸세요..</p>
        <a href="https://browsehappy.com/">업데이트하러 가기</a>
      </video>

      <!-- iframe -->
      <!-- 직접 쓸 경우는 거의 없다. 다른 곳에서 퍼올 때 쓰이기도 한다. -->
    </video>
  </audio>
  ```

- 기타 Etc

  ```html
  <!-- abbreviation약자 -->
  <p>
    너..혹시
    <abbr title="Attention Deficit Hyperactivity Disorder">ADHD</abbr>니?
  </p>

  <!-- address -->
  <address>
    <h1>최문경</h1>
    <a href="">깃허브</a>
  </address>

  <!-- preformatted text, code -->
  <pre>
    ㅇ ㅏ ㄴ ㅕ ㅎ ㅏ ㅅ ㅔ ㅇ
      ㄴ    ㅇ             ㅛ
  </pre>

  <pre>
    <code>
      <!-- 코드 작성(code태그만 써서 code를 작성해도 상관없음) -->
    </code>
  </pre>
  ```

- Doctype & Documnet Structure

  ```html
  <!-- 브라우저야, 이 문서는 HTML5 버전으로 작성된 문서야  그러니까 그에 맞춰서 렌더링 해줘~ -->
  <!-- DOCTYPE == document type -->
  <!DOCTYPE html>
  <html>
    <head></head>
    <body></body>
  </html>
  ```

- title, link, style, script

  - spoqa han sans글씨체 괜찮은듯
  - script는 head보다 body가 끝나기 직전에 쓰는게 더 좋은 이유? link와 달리 script는 script파일을 모두 읽어오기전까지는 body안의 내용을 읽지 않아서 비효율적이다.

- meta
  - 필수 attribute: `name`과 `content`
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="author" content="denomoon" />
  <meta name="keywords" content="html, css, js" />
  <meta name="description" content="html을 공부하고 정리해보았습니다." />
  ```
