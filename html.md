# HTML(Hyper Text Markup Langauge)

## - HTML Tag Basic Syntax

### 1. 기본 형식

```
<태그>콘텐츠</태그>
```

```
<div>Hello world</div>
```

### 2. 속성을 가지는 형식

```
<태그 속성1="값" 속성2="값">콘텐츠</태그>
```

```
<a href="https://www.google.com">Google</a>
```

### 3. 태그 안에 태그를 가지는 형식

```
<div>
    <p>Hello word</p>
</div>
```

### 4. 콘텐츠가 없는 형식

```
<태그 속성="값" />
```

```
<br />
<img src="" />
```

### 5. HTML 주석

```
<!-- 주석입니다 -->
```

## - HTML Basic Construction

```
<html>
    <head>
        <!-- 콘텐츠를 보여주는 것 이외의 모든 설정 태그를 넣습니다. -->
    </head>
    <body>
        <!-- 실제로 화면을 구성하는 태그를 넣습니다. -->
    </body>
</html>
```

## - HTML TAG

```
<name attribute="value"> content </name>
```

### 1. META tag

- meta: 엑스트라, 추가 정보를 담습니다.
- 유저를 위한 정보가 아닌 브라우저를 위한 정보를 담습니다.
- head 파트에 작성됩니다.

### 2. Sementic tag

- 뜻, 의미가 있는 태그입니다.
- article, title, ...

### 3. Non-Sementic tag

- 아무 지칭하는 바, 의미가 없는 태그입니다.
- div, p, ...

## - HTML 주요 태그

### 1. h1, h2, h3, h4, h5, h6

: headline의 약자로 일밙거으로 제목을 표시할 때 사용하는 태그입니다.

1. 줄바꿈 : O
2. 기본 너비 : 부모너비

### 2. p

: 일반적으로 문단(paragraph)을 나눌 때 사용하는 태그입니다. 일반 텍스트를 표시할 때 주로 사용합니다.

1. 줄바꿈 : O
2. 기본 너비 : 부모 너비

### 3. br

: 줄바꿈을 할 때 사용하는 태그입니다.

### 4. a

: 다른 링크로 넘어가도록 돕는 태그입니다. 필수 속성으로 href="넘어갈 주소" 를 적어야 합니다.

1. 줄바꿈 : X
2. 기본 너비 : 콘텐츠 너비

### 5. img

: 이미지를 보여주는 태그입니다. 필수 속성으로 src="이미지 주소" 를 적어야 합니다. alt 속성은 img가 제대로 보여지지 않았을 때 보여지게 될 문구입니다.

1. 줄바꿈 : X
2. 기본 너비 : 이미지 너비

### 6. form, input

: form 태그는 내부에 입력하는 값들을 관리해주는 태그 입니다. form의 주요 속성 중 action은 submit event 발생 시 서버 url로 정보를 전송합니다.

form 태그 안에는 input 태그들이 들어갑니다. type 속성을 통해 text, password, radio, file, submit 등을 넣을 수 있습니다.

label 태그는 input 태그의 라벨을 붙을 때 사용합니다.

### 7. div

: 영역을 나누도록 도와주는 태그입니다.

1. 줄바꿈 : O
2. 기본 너비 : 부모 너비

### 8. span

: div 와 함께 CSS 를 이용해서 영역을 구성할 때 많이 사용합니다.

1. 줄바꿈 : X
2. 기본 너비 : 콘텐츠 너비

## 태그에 이름 짓는 법

- ID : 고유한 element를 사용할 때 적용합니다.
- Class : 고유하지 않은, 계속 반복되느 element의 경우 적용합니다.
