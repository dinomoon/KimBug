# CSS는 재밌다.

### Box Sizing

- box-sizing의 기본값은 content-box;인데 width와 heignt를 주면 content만의 너비와 높이를 가지고 정하기 때문에 padding과 border를 줬을 때 우리가 의도했던 사각형의 길이와 높이가 아닐 수 있다. padding과 border까지 포함해서 사각형의 너비와 높이를 인지하는 우리의 상식과는 맞지 않으므로 border까지 포함해서 길이와 너비를 알아서 맞춰주는 box-sizing: border-box;를 처음에 써주자.

```css
* {
  box-sizing: border-box;
}
```

### Box

- 모든 태그들은 display속성을 가지고 있다. 그리고 display속성의 값은 block, inline, inline-block, flex, grid가 있다.
- Block -> 길막!
  1. width값을 주지 않으면 부모의 width만큼 가진다.
  2. width값을 줘도 나머지 부분을 자동으로 margin으로 채운다.
  3. margin-left: auto를 했을 때 오른쪽으로 이동하는 것은 자동으로 생긴 auto마진을 왼쪽에 주기때문이다. -> margin: 0 auto;를 하면 자동으로 생긴 auto마진을 왼쪽 오른쪽에 나눠 갖기 때문에 가운데 정렬이 되는 것이다.
  4. height값을 주지 않으면 자기 자신의 컨텐츠 또는 자식의 높이 만큼 height가 잡힌다.
- width, height, padding, margin 모두 사용할 수 있다.

### Inline

- inline -> 흐름
- width, height, padding-top, padding-bottom, margin-top, margin-bottom을 사용할 수 없다!

### inline-block

- inline과 block의 장점을 가지고 있는 녀석
- 흐름과 영역을 동시에 잡을 수 있다.

### float

- 지금은 거의 쓰지 않지만 옛날 코드를 이해해야 하는 상황도 올 수 있으니 알아두자.

1. 집나간 내 새끼, 찾을 길 없네 (부모의 높이 또는 너비가 float한 요소의 높이 또는 높이 만큼 줄어든다.)
2. 블록으로 신분상승 (inline요소에 float를 주면 block이 된다.)
3. 길막을 못해 슬픈 블록아! (float을 주면 자동으로 생기던 auto마진이 더 이상 생기지 않는다.)
4. 플로트, 나만 볼 수 있어요(feat.인라인) (인라인 요소는 float요소를 알아보고 옆에 배치 된다.)

- 부모요소에 overflow: hidden; 을 사용하거나 ::after {content:''; display:block; clear:both;}를 사용하면 부모의 높이가 잡힌다.

### position

- static(기본값), relative, absolute, fixed, sticky
- relative

  - 원래 있던 자리를 기준으로 움직인다.
  - 원래 있던 자리를 비워놓지 않는다.(다른 요소들이 침범하지 않음)

- absolute

  - 부모 요소 중에서 static이 아닌 position을 가진 부모를 기준으로 움직인다.
  - float과 똑같은 특징을 가진다.(4번빼고) 인라인 요소도 absolute를 못알아본다.

- fixed
  - viewport를 기준으로 움직인다.

### flex

1. 나, 플렉스 박스 쓸거임
2. 가로 정렬? 세로 정렬?
3. 무조건 한 줄 안에 다 정렬?
   - nowrap 무조건 한 줄안에 정렬
   - wrap 너비만큼 알아서 정렬

### 타이포그래피, typography

- 디자인에 있어서 활자의 서체나 글자 배치 등의 구성 및 표현.
- font-size
  - px(절대단위), em(상대단위), rem(상대단위)
  - em = equal to capital M (요소안에 적용된 폰트 사이즈의 배수)
  - rem = root em = html em (html 폰트 사이즈의 배수)
- line-height
  - line-height: 1.5(em); px과 rem은 적어주지만 em은 생략해주는 것이 관례 (대부분의 경우에 em을 사용한다.)
- letter-spacing

  - 글자 간격(자간) em을 대부분 사용, 하지만 line-height와는 다르게 em을 생략하면 안된다.

- font-family

  - font-family: Roboto, Poppins, sans-serif; (Roboto없으면 Poppins, Poppins도 없으면 sans-serif체 중에서 아무거나를 font로 해달라)
  - 서체명이 한글이거나 띄어쓰기가 있는 경우 반드시 따옴표로 감싸줘야한다.
  - serif: 꺾쇠가 있는 글씨체 (바탕체, 궁서체, 명조체)(줄의 연속성을 주어서 가독성을 높임)
  - sans-serif: sans는 프랑스어로 없음을 뜻한다. 따라서 꺾쇠가 없는 서체를 말한다. (고딕체)(serif에 비해 깔끔하고 세련된 느낌)

- font-weight
  - 400: Regular, 700: bold
- color

  - hex, rgb, rgba

### background

- background-color
- background-image
- background-repeat
- background-size
  - contain, cover, custom
- background-position

### final project

- page Layout

  - 반드시 container안에는 row만! 그리고 row안에는 col-만!! 다른 것들이 들어가면 나중에 스타일이 꼬일 수 있다.(bootstrap때문에)

- `작업환경세팅`

  - 항상 시작하기 전에 무작정 덤비지 말고 한 템포 쉬어서 작업환경부터!
  - 필요한 css, assets가져오고 reset하기!
