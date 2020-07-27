# Markup(HTML/CSS) Style Guide

아래 내용은 [여기](https://codeguide.co/)를 참고하여 작성했습니다.

## HTML

### HTML5 Doctype

```html
<!DOCTYPE html>
```

### 기본 템플릿

```html
<!DOCTYPE html>
<html>
    <head>
        <!-- HTML 문서에 대한 메타 정보 -->
    </head>
    <body>
        <!-- HTML 문서 본문 내용 -->
    </body>
</html>
```

### 문서의 언어 속성

[여기](https://www.sitepoint.com/iso-2-letter-language-codes/)에서 나온 언어 코드로 지정 가능하다.

```html
<html lang="ko">
    <!-- ... -->
</html>
```

### IE 호환성 모드

```html
<head>
    <meta http-equiv="x-ua-compatible" content="ie=edge" />
</head>
```

### 문자 인코딩

기본적으로 "UTF-8" 인코딩을 사용한다.

```html
<head>
    <meta charset="utf-8" />
</head>
```

### CSS / JavaScript 삽입

```html
<head>
    <!-- 외부 CSS -->
    <link rel="stylesheet" href="style.css" />

    <!-- 해당 문서 적용 CSS -->
    <style>
        /* ... */
    </style>

    <!-- 자바스크립트 -->
    <script src="example.js"></script>
</head>
```

### 속성 순서

HTML 요소의 속성은 가독성을 위해 다음 순서대로 지정한다.

-   class
-   id, name
-   data-\*
-   src, for, type, href, value
-   title, alt
-   role, aria-\*

class 속성은 재사용성을 위해 가장 우선하며, id 속성은 비교적 구체적이고 드물게 사용하기 때문에 두번째로 우선한다.

```html
<a class="..." id="..." data-toggle="modal" href="#">
    Example link
</a>

<input class="form-control" type="text" />

<img src="..." alt="..." />
```

### Boolean 속성

Boolean 속성은 값을 지정하지 않는다.

```html
<input type="text" disabled />

<input type="checkbox" value="1" checked />

<select>
    <option value="1" selected>1</option>
</select>
```

### 마크업 줄이기

가능하면 불필요한 상위 요소를 만들지 말 것. HTML은 최대한 간결하게 작성한다.

```html
<!-- 불필요한 상위 요소 -->
<span class="avatar">
    <img src="..." />
</span>

<!-- 간결한 마크업 -->
<img class="avatar" src="..." />
```

### JavaScript로 마크업 생성하기

JavaScript로 마크업을 작성하면 내용을 찾기 어렵고, 편집하기도 어렵고, 성능도 떨어지므로 `가능하면 피할 것`.
