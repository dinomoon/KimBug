# HTML 훈련

### Feature Box

![그림](https://user-images.githubusercontent.com/19285811/69003607-2914b000-0940-11ea-8f44-c82f9540df2b.png)

- 이미지가 정보로서 의미가 없다고 생각한다면 img태그를 사용해 이미지를 나타내지 않고 css를 사용해 이미지를 나타내는 것도 좋다.

```html
<!-- Without Image Tag -->
<div class="feature-box no-image">
  <h1>
    Free unlimited private repositories
  </h1>
  <p>
    Free for small teams under 5 and priced to scale with Standard (<span
      aria-label="3 Dollars per user per month"
      >&dollar;3/user/mo</span
    >) or Premium (<span aria-label="6 Dollars per user per month"
      >&dollar;6/user/mo</span
    >) plans.
  </p>
</div>
```

### Logo in header

![사진](https://user-images.githubusercontent.com/19285811/69004168-abee3880-0949-11ea-93a0-291797349fa7.png)

- 로고가 헤더안에 있을 때

```html
<div class="header">
  <h1>
    <a href="./index.html">
      <img
        src="https://statics.goorm.io/logo/edu/goorm_edu.svg"
        alt="구름 Edu"
      />
    </a>
  </h1>
  <a href="https://edu.goorm.io/qna">Q&amp;A</a>
</div>
```

### Breadcrumb & Pagination

![사진](https://user-images.githubusercontent.com/19285811/69315201-f1c03f00-0c70-11ea-9e42-b0403d458574.png)

- breadcrumb사이의 슬래시는 css가상선택자로 만듦.
- wai-aria를 사용해 장애인들에게 더 정확한 정보를 전달할 수 있다.

```html
<div class="breadcrumb">
  <a href="https://github.com/rohjs">rohjs</a>
  <a href="https://github.com/rohjs/bugless-101">bugless-101</a>
</div>

<div class="pagination">
  <a href="#" class="disabled" aria-label="Go to previous page">Previous</a>
  <ol>
    <li class="current-page">
      <a href="#" aria-label="Current page. Page 1">1</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 2 page">2</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 3 page">3</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 4 page">4</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 5 page">5</a>
    </li>
    <li>
      <button type="button" disabled>...</button>
    </li>
    <li>
      <a href="#" aria-label="Go to 6 page">6</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 7 page">7</a>
    </li>
    <li>
      <a href="#" aria-label="Go to 8 page">8</a>
    </li>
  </ol>
  <a href="#" aria-label="Go to next page">Next</a>
</div>
```
