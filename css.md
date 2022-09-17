# 👍 CSS(Cascading Style Sheets)

<br>

## ⚡ HTML과 CSS를 연결하는 방법

### 1. inline

: html 문서 내부에서 style을 작성하는 방법입니다. html 파일마다 계속 복사, 붙여넣기를 반복해야하기 때문에 비효율적일 수 있습니다.

```
<html>
    <head>
        <style type="text/css">
            /* 이 곳에 CSS를 작성합니다. */
        </style>
    </head>
```

### 2. external

: 외부 파일을 불러오는 방식으로, style.css 파일을 연결만 하고 파일 내용을 변경하면 자동으로 연결된 모든 html 문서에 적용되는 방법입니다.

```
<html>
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
```

<br>

## ⚡ CSS Basic Syntax

```
선택자 {
    속성: 값;
    속성: 값;
}
```

### 1. 선택자(Selector)

: 선택자는 스타일을 적용할 대상입니다. 태그, ID, Class 등을 선택할 수 있습니다.

```
/* 태그를 선택자로 했을 때 */
p {
    color: red;
}

/* 태그를 ID로 했을 때 */
#title {
    color: blue;
}

/* 태그를 Class로 했을 때 */
.item {
    color: green;
}
```

- ID 는 고유한 값으로, 딱 한 요소에게만 적용됩니다.
- Class 는 Class 가 적용된 모든 요소에게 적용됩니다.

### 2. 복합 선택자

: 태그, id, class 가 기본 선택자라고 한다면 이들을 결함합 선택자를 복합 선택자라고 합니다. 복합 선택자로는 하위 선택자(Descendant Selector)와 자식 선택자(Child Selector) 등이 있습니다.

### 2-1. 하위 선택자 (Descendant Selector)

: `선택자 a 선택자 b` 로 띄어쓰기를 통해서 구분해줍니다. 하위 선택자는 상위 선택자(선택자 a) 내부에 있는 모든 요소들 중 하위 선택자(선택자 b)에 해당하는 태그를 선택합니다.

### 2-2. 자식 선택자 (Child Selector)

: `선택자 a > 선택자` 로 >를 통해서 구분해줍니다. 자식 선택자는 상위 선택자(선택자 a)의 내부에서 가장 바깥에 있는 태그들 중에서 하위 선택자(선택자 b)에 해당하는 태그를 선택합니다.

<br>

## ⚡ Pseudo Selector, 가상 셀렉터

: 셀렉터인데 element가 아닌 것입니다. 즉, 태그 이름이나 class, id를 쓰지 않고 선택하는 방법입니다.

```
selector:pseudo-selector {
    속성: 값;
}
```

### 1. CSS states

: 가상 셀렉터로는 다음과 같은 특정 상태에 따라 스타일을 정의할 때 사용합니다.

- hover: 해당 박스 위에 뭔가 올라가면(hover) 상태가 변합니다.
- active: 해당 박스를 클릭할 때 상태가 변합니다.
- focus: 포커싱 될 때 상태가 변합니다.
- visited: 방문한 적이 있을 때 상태가 변합니다.

<br>

## ⚡ Transitions, 트랜지션

: 이름/변경을 멋있게 보여주는 효과입니다. 어떤 state가 바뀔 때 적용합니다. (focus, active, hover에서 효과적으로 적용됩니다.)

<br>

## ⚡ Trasformations, 트랜스포메이션

: html 문서의 element들을 변경, 모습이 변하는 효과를 줍니다.

<br>

## ⚡ Animatinos, 애니메이션

: state할 필요없이 계속 효과가 발생하기 원할 때 사용합니다.

### 1. 스테이지가 2개일 때,

```
@Keyframe nameOfAnimation {
    from {
        ...
    }
    to {
        ...
    }
}
```

### 2. 스테이지가 3개일 때,

```
@Keyframe nameOfAnimation {
    0% {
        ...
    }
    50% {
        ...
    }
    100% {
        ...
    }
}
```

<br>

## ⚡ Media Query, 미디어 쿼리

: 모바일-데스크탑 환경에 따라서 반응형 웹 디자인을 할 때 사용합니다. 브라우저 사이즈를 잡습니다. (@media)

<br>

## ⚡ CSS 주요 속성

### 1. 크기

: 크기는 웹의 기본 단위인 px, 혹은 부모 태그의 크기를 기준으로 한 %가 있습니다.

- width: 선택자 태그의 너비
- height: 선택자 태그의 높이

```
#item {
    width: 300px; /* 웹에서 px은 크기의 기본 단위입니다. */
    height: 30%; /* 부모의 크기 대비 30%를 차지합니다. */
}
```

### 2. 색상

: 색상은 CSS에서 기본으로 설정되어 있는 예약 색상(red, blue 등)과 rgb로 표현됩니다.

- color: 폰트의 색상을 정하는 속성
- background-color: 선택자 태그의 배경색을 정하는 속성

```
#item {
    color: red; /* red, blue 등 css에서 이미 예약된 색상입니다. */
    color: rgb(255,0,0); /* rgb는 색상을 표현하는 표준 색상값입니다. */
    color: #ff0000; /* rgb를 16진수 형태로 표시할 수도 있습니다. */
    background-color: red;
}
```

### 3. 폰트

- font-size: 선택자 안에 있는 텍스트의 크기를 정하는 속성 (단위: px)
- font-weight: 선택자 안에 있는 텍스트의 굵기를 정하는 속성 (100 ~ 900)

```
#item {
    font-size: 32px;
    font-weigh: 500;
}
```

### 4. Box Model

- Margin : 여백 (선택자의 바깥의 여백을 설정합니다.)
- Border : 테두리 (태그의 테두리에 선을 적용하는 속성입니다.)
- Padding : 여백 (선택자의 내부의 여백을 설정합니다.)
- Content : 내용

```
#item {
    margin: 10px /* 상하좌우 모두 margin 10px이 적용됩니다. */
    margin-right: 10px /* 오른쪽에 margin 10px이 적용됩니다. */
    padding: 0 10px 0 0; /* 순서대로 상 우 좌 하 에 padding 값을 적용합니다. */
    border: 1px solid #ff0000; /* 너비(1px), 스타일(실선), 색상(빨강)을 적용합니다. */
}
```

<br>

## ⚡ Display

### 1. Inline

: 폭-높이 박스 없이 서로 옆에 붙는 형태(Text)입니다.

### 2. Inline-Box

: 박스들이 서로 옆에 붙는 형태입니다.

### 3. Block

: 박스들이 밑에 붙는 형태입니다.

<br>

## ⚡ Position

### 1. static

: 디폴트 값잆니다.

### 2. fixed

: 고정, 어디든 오버랩해서 계속 해당 위치에 고정시키기 위한 방법입니다.

### 3. absolute

: 포지션 relative에 상대적으로 포지션을 잡는 형태입니다. relative 포지션이 없을 경우, absolute는 문서의 본문 body에 맞춰서 포지션을 잡습니다.

### 4. relative

<br>

## ⚡ Display : flex

### 컨테이너(부모) 속성

: 해당 속성은 부모 클래스에만 적용하면 됩니다.

### 1. flex-direction

: 자식의 정렬 방향을 설정합니다. row는 수평으로, column은 수직으로 정렬합니다.

```
.parent {
    display: flex;
    flex-direction: column; /* 기본값은 row입니다. */
}
```

### 2. justify-content

: 아이템 정렬 방향(by flex-direction)과 같은 방향으로 아이템의 여백을 관리할 때 설정합니다. flex-direction이 row이면 수평으로, flex-direction이 column이면 수직으로 배치됩니다. 기본 값은 flex-start입니다.

- flex-start
- flex-end
- center
- space-around
- space-between

```
.parent {
    display: flex;
    justify-content: center;
}
```

### 3. align-items

: 아이템 정렬 방향(by flex-direction)과 수직 방향으로 아이템의 여백을 관리할 때 설정합니다. flex-direction이 row이면 수직으로, flex-direction이 column이면 수평으로 배치됩니다. 기본값은 stretch입니다.

- stretch
- flex-start
- flex-end
- center
- baseline

```
.parent {
    display: flex;
    align-items: center;
}
```

### 4. flex-wrap

: 아이템이 컨테이너를 넘어섰을 때 어떻게 처리할 것인지 설정합니다. 기본 겂은 nowrap으로 부모의 크기(너비 or 높이)를 기준으로 자식들이 알아서 공간을 나눠서 나열됩니다. 즉, 줄바꿈이 일어나지 않습니다. 많은 아이템들을 보여줘야 할 때 flex-wrap 속성에 wrap을 부여하면 알아서 줄바꿈이 일어납니다.

```
.parent {
    display: flex;
    flex-wrap: wrap;
}
```

### 5. flex-flow

: flex-direction + flex-wrap

```
.parent {
    display: flex;
    flex-flow: row wrap;
}
```

### 아이템(자식) 속성

### 6. flex-basis

: 자식의 최소 너비를 설정할 떄 사용합니다. 수직 정렬일 때는 높이를 설정합니다. 기본 값은 auto입니다.

### 7. flex-glow

: Container에 여백이 생겼을 때 아이템이 어떻게 영역을 차지할지 설정합니다. 다른 아이템들과 비교해서 해당 비율로 여백을 가져갑니다. 기본 값은 0입니다.

### 8. flex-shrink

: Container가 자식들이 차지하는 공간보다 줄어들었을 때 너비를 어떤 비율로 줄일지 정합니다. 다른 아이템들과 비교해서 해당비율로 줄어들게 됩니다. 기본 값은 1입니다.

<br>
