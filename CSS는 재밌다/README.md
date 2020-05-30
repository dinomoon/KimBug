# CSS는 재밌다.

### Box Sizing

- box-sizing의 기본값은 content-box;인데 width와 heignt를 주면 content만의 너비와 높이를 가지고 정하기 때문에 padding과 border를 줬을 때 우리가 의도했던 사각형의 길이와 높이가 아닐 수 있다. padding과 border까지 포함해서 사각형의 너비와 높이를 인지하는 우리의 상식과는 맞지 않으므로 border까지 포함해서 길이와 너비를 알아서 맞춰주는 box-sizing: border-box;를 처음에 써주자.

```css
* {
  box-sizing: border-box;
}
```
