
# 웹 개발 기초 강의 자료

## 1. HTML 기본 개념
HTML은 웹 페이지를 만들기 위한 언어입니다. 웹 페이지의 구조를 나타내는 역할을 합니다.

### HTML 구조
HTML 문서는 다음과 같은 기본 구조로 이루어져 있습니다:

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>내 웹사이트</title>
</head>
<body>
    <!-- 여기에 웹 페이지의 내용이 들어갑니다 -->
</body>
</html>
```

### 주요 태그
- `<html>`: 문서의 시작과 끝을 나타냅니다.
- `<head>`: 메타 정보, 스타일 시트, 스크립트 등이 포함됩니다.
- `<title>`: 페이지의 제목을 설정합니다.
- `<body>`: 실제로 화면에 표시될 내용을 포함하는 부분입니다.

---

## 2. HTML 태그
여러 HTML 태그를 사용해 웹 페이지를 만들어보겠습니다: `<div>`와 `<a>`.

### 2.1 `<div>` 태그
`<div>` 태그는 웹 페이지에서 구역을 나누는 용도로 사용됩니다. 웹 페이지의 다양한 요소를 그룹화할 수 있습니다.

```html
<div>
    여기에 본인 소개 내용을 작성하세요.
</div>
```

### 2.2 `<a>` 태그
`<a>` 태그는 링크를 만들 때 사용됩니다. 웹 페이지 내에서 다른 페이지로 이동할 수 있게 하거나, 외부 웹 사이트로 연결할 수 있습니다.

```html
<a href="https://www.example.com">내가 좋아하는 사이트로 이동</a>
```

### 2.3 `<p>` 태그
`<p>` 태그는 문단(Paragraph)을 나타내는 태그입니다. 긴 글이나 설명을 작성할 때 사용합니다.

```html
<p>여기에 문단 내용을 작성하세요.</p>
```

### 2.4 `<span>` 태그
`<p>` 태그는 인라인 요소로, 짧은 텍스트나 구문에 스타일을 적용할 때 사용합니다. (문장 내에서 특정 단어나 구문을 강조할 때 유용합니다.)

```html
<p>저는 <span style="color: red;">빨간색</span>을 좋아합니다.</p>
```

---

## 3. CSS로 스타일 적용하기
CSS는 웹 페이지의 스타일을 지정하는 언어입니다. HTML만으로는 웹 페이지가 너무 기본적인 형태이므로 CSS를 사용해 스타일을 입혀보겠습니다.

### CSS 기본 문법
```html
<style>
    div {
        background-color: lightgray;
        padding: 10px;
        margin: 10px;
        border-radius: 5px;
    }
    
    a {
        color: blue;
        text-decoration: none;
    }

    a:hover {
        color: red;
    }
</style>
```

이 코드는:
- `<div>` 태그에 배경색과 여백을 추가합니다.
- `<a>` 태그에 링크 색상을 지정하고, 마우스를 올렸을 때 색상이 변하도록 합니다.

---

## 4. JavaScript 기본 개념
JavaScript는 웹 페이지에 동적인 기능을 추가할 수 있는 언어입니다. 간단한 예제를 통해 JavaScript가 어떻게 동작하는지 알아보겠습니다.

### 클릭 시 알림창 띄우기
```html
<script>
    function showAlert() {
        alert('안녕하세요!');
    }
</script>

<button onclick="showAlert()">클릭하세요</button>
```

이 코드는 버튼을 클릭하면 알림창이 뜨는 간단한 기능을 구현합니다.

---

## 5. 실습: 나만의 웹사이트 만들기

### Step 1: HTML 구조 만들기
먼저 HTML 기본 구조를 만듭니다.

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>나의 소개 페이지</title>
</head>
<body>
    <div>
        <h1>안녕하세요, 저는 [여기에 이름을 쓰세요]</h1>
        <p>저는 [본인 소개 내용을 여기에 작성하세요]</p>
    </div>
    <div>
        <a href="https://www.example.com">내가 좋아하는 사이트</a>
    </div>
</body>
</html>
```

### Step 2: CSS 적용하기
스타일을 추가해 페이지를 좀 더 보기 좋게 만듭니다.

```html
<style>
    body {
        font-family: Arial, sans-serif;
        line-height: 1.6;
    }

    div {
        background-color: lightyellow;
        padding: 20px;
        margin: 15px;
        border-radius: 10px;
    }

    a {
        color: green;
        text-decoration: underline;
    }

    a:hover {
        color: orange;
    }
</style>
```

### Step 3: JavaScript 추가하기
간단한 버튼을 추가해 페이지에 상호작용 기능을 넣어봅니다.

```html
<script>
    function introduce() {
        alert('안녕하세요, 저는 [여기에 이름을 쓰세요]입니다!');
    }
</script>

<button onclick="introduce()">소개 버튼</button>
```

---

## 6. 마무리
이 강의를 통해 간단한 HTML, CSS, JavaScript를 사용해 자신만의 웹 페이지를 만들어 보았습니다. 각자 A4 용지에 그린 웹 페이지 디자인을 바탕으로, 직접 코드를 작성하고 본인만의 멋진 웹사이트를 만들어보세요!
