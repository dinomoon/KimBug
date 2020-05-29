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
- em은 좀 더 주관적이고, strong은 좀 더 객관적인 중요성을 의미한다.

  ```html
  <p>
    그 치킨의 가격은 <strong>20,000원</strong>이었지만,
    <em>매우 맛이 없었습니다.</em>
  </p>
  ```

**링크 Anchor**

- href속성의 값으로 가능한 것들
  - 웹 URL
  - 페이지 내 이동
  - 메일주소
  - 전화번호
  ```html
  <a href="https:www.naver.com"></a>
  <a href="#section2"></a>
  <!-- <section id='section2'></section>-->
  <a href="mailto:ansrud1003@naver.com"></a>
  <a href="tel:01012345678"></a>
  ```
- target = "\_blank" 새 창으로 열기
  > 하지만 이 target 속성은 권장되는 속성은 아닙니다. 왜냐하면 이 링크를 현재페이지에서 열 지, 새 창으로 열 지는 사용자의 선택이기 때문입니다. 따라서, 웬만하면 target 속성은 자제하시기 바랍니다. (webber study)
- rel 속성을 통해서 해당 링크와의 관계를 나타낼 수 있다.
  - `alternate` 대안 페이지 (프린트 페이지 또는 번역된 페이지 등등)
  - `author` 저자에 대한 페이지
  - `bookmark` 즐겨찾기 추가를 위한 고유링크
  - `help` 현재 페이지에 대한 도움말 페이지
  - `license` 현재 페이지에 대한 저작권 페이지
  - `prev` 이전 글
  - `next` 다음 글
  - `search` 검색 페이지
    > 이 rel 속성을 넣어도 브라우저에서 특별히 표시되지 않습니다. 하지만, 이 속성 역시 검색엔진이 활용하므로 적어주는 것이 좋습니다. (webber study)

**이미지 Image**

> 우리가 보통 알고 있는 이미지 포맷에는 gif, jpg, png가 있습니다. 각 포맷의 특징을 잘 모르고 사용하는 경우가 많습니다. 심지어 이미지를 주로 다루는 웹 디자이너 중에서도 은근 잘 모르고 사용하는 경우가 많습니다. 특히 이미지는 웹 페이지 내에서 차지하는 용량이 매우 크기 때문에, 이미지 포맷을 효율적으로 사용하지 않으면 웹 페이지가 매우 무거워 질 수 있습니다. 참고로 이미지 포맷이라는 것은 이미지를 압축하는 방식을 말합니다. (webber study)

- 이미지 태그는 src와 alt 두개의 속성을 모두 적어줘야한다.
- alt속성은 alternate의 줄임말로, src의 주소가 잘못되었거나 해당 주소의 서버에 문제가 있어서 이미지를 불러오지 못했을 때 이미지 대신 보여주는 대체 텍스트이다. 그리고 스크린리더에서는 alt의 값을 읽어준다고 한다. ex) '고양이와 강아지 이미지'
  - 텍스트 이미지의 경우 해당 텍스트를 반드시 포함해야 한다.
- title속성은 툴팁을 나타낸다.

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

- dt는 인라인 요소이며, dd는 블럭 요소입니다. 때문에 dt 안에 블럭 요소를 안된다.
- dt와 dd는 1:1 형태가 아닌, 1:다, 다:1, 다:다의 형태를 취할 수 있다.

```html
<!-- 출처: webber study -->
<dl>
  <dt>한글</dt>
  <dd>
    우리나라 글자의 이름. 1445년에 훈민정음이라는 이름으로 반포되었다.
  </dd>
</dl>

<!-- 출처: webber study -->
<!-- 목록의 중복 사용 -->
<h1>라면 레시피</h1>
<dl>
  <dt>준비물</dt>
  <dd>
    <ul>
      <li>물 550cc</li>
      <li>라면봉지</li>
    </ul>
  </dd>

  <dt>조리법</dt>
  <dd>
    <ol>
      <li>물을 끓인다.</li>
      <li>물이 끓으면, 면과 스프를 넣는다.</li>
      <li>다 익으면 불을 끄고 맛있게 먹는다.</li>
    </ol>
  </dd>
</dl>

<!-- dfn예시 -->
<p>
  A <dfn id="def-validator">validator</dfn> is a program that checks for syntax
  errors in code or documents.
</p>

<!-- webber story -->
<p><dfn>언감생심</dfn>은 감히 바랄 수도 없다는 뜻의 사자성어입니다.</p>
<!-- 또는 -->
<p>
  <dfn><abbr title="Hyper Text Markup Language">HTML</abbr></dfn
  >은 웹 페이지 작성을 위한 마크 업 언어입니다.
</p>
```

**인용 Quotations**

- blockquote태그와 q태그가 존재한다.
- blockquote태그는 하나의 문단 자체나 문장이 인용되었을 때, q태그는 문단 안에서 어떤 문장이 인용되었을 때 사용한다.
  - blockquote의 cite속성은 인용한 사이트의 url, cite태그는 작품 제목을 쓸 때 사용한다. (사람의 이름X)
  - q태그는 큰따옴표를 자동으로 생성해준다.

```html
<p>다음은 소설 <cite>소나기</cite>의 한 부분입니다.</p>
<blockquote cite="http://example.com/">
  <p>'이 바보.'</p>
  <p>조약돌이 날아왔다. 소년은 저도 모르게 벌떡 일어섰다.</p>
</blockquote>
```

**흑마법 Div & Span**

- 아무런 의미를 가지고 있지 않다. 오로지 스타일링을 위한 태그이다.
  > 정말 아무리 생각해도 떠오르는 태그가 없을 때 사용...

**Form**

- 반드시 써야하는 속성 2가지 -> action과 method
  - action은 form을 처리할 곳으로 보내는 주소를 적고 method는 처리할 방식을 적는다.(GET또는 POST)
  - name 속성은 데이터가 서버로 전송될 때 할당되는 변수의 이름이다.
- input

  ```html
  <form action="" method="GET">
    <input
      type="text"
      name="id"
      placeholder="아이디를 입력하세요"
      minlength="5"
      maxlength="13"
      required
    />
    <input
      type="text"
      name="name"
      placeholder="이름을 입력하세요"
      minlength="5"
      maxlength="13"
      value="최문경"
      disabled
    />
    <input type="email" placeholder="이메일을 입력하세요" />
    <input
      type="password"
      name="password"
      placeholder="비밀번호를 입력하세요"
      minlength="6"
      maxlength="14"
    />
    <input type="url" name="url" placeholder="포트폴리오 url을 입력하세요" />
    <input
      type="number"
      name="age"
      placeholder="10~20사이의 수를 적으세요"
      min="10"
      max="20"
    />
    <input type="file" name="file" accept=".jpg, .png" />
  </form>
  ```

- label

  > 웹 접근성 기준 상, 폼 입력 요소가 있다면 이에 해당하는 label 요소를 반드시 가지고 있어야 합니다. 만약 label을 넣을만한 공간적인 여유가 없거나 부득이한 경우라면, 해당 폼 입력 요소에 title 속성이라도 넣도록 권장하고 있습니다.

  ```html
  <form action="" method="GET">
    <label for="user-id" />
    <input id="user-id" type="text" required placeholder="아이디" name="id" />
  </form>

  <!-- 화면에 label을 넣을 공간이 없습니다. -->
  <input type="text" title="아이디 입력" />
  <!-- title 속성으로라도 명시를 해주어야 합니다. -->
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
    <caption>
      시간표
    </caption>
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
