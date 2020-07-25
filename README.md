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