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
