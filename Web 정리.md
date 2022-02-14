# HTML

### DOM

텍스트 파일인 HTML 문서를 브라우저에서 렌더링 하기 위한 구조

- HTML 문서에 대한 모델을 구성함
- HTML 문서 내의 각 요소에 접근 / 수정에 필요한 프로퍼티와 메서드를 제공함
- 트리 구조를 가지고 있다. 부모-자식관계, 형제 관계



### 요소(element)

- HTML 요소는 시작 태그와 종료 태그 그리고 태그 사이에 위치한 내용으로 구성
  - 태그(Element, 요소)는 컨텐츠(내용)를 감싸는 것으로 그 정보의 성격과 의미를 정의한다.

- 내용이 없는 태그들
  - br, hr, img, input, link, meta
- 요소는 중첩될 수 있음
  - 요소의 중첩을 통해 하나의 문서를 구조화
  - 여는 태그와 닫는 태그의 쌍을 잘 확인해야함
    - 오류를 반환하는 것이 아닌 그냥 레이아웃이 깨진 상태로 출력되기 때문에, 디버깅이 힘들어 질 수 있다.
- 모든 HTML 요소가 공통으로 사용할 수 있는 대표적인 속성 (몇몇 요소에는 아무 효과가 없을 수 있음)
  - id : 문서 전체에서 유일한 고유 식별자 지정
  - class : 공백으로 구분된 해당 요소의 클래스의 목록 (CSS, JS에서 요소를 선택하거나 접근)
  - data-* : 페이지에 개인 사용자 정의 데이터를 저장하기 위해 사용
  - style : inline 스타일
  - title : 요소에 대한 추가 정보 지정
  - tabindes : 요소의 탭 순서



### 시맨틱 태그

- HTML5에서 의미론적 요소를 담은 태그의 등장
  - 기존 영역을 의미하는 div 태그를 대체하여 사용
- 대표적인 태그 목록
  - header : 문서 전체나 섹션의 헤더(머리말 부분)
  - nav : 내비게이션
  - aside : 사이드에 위치한 공간, 메인 콘텐츠와 관련성이 적은 콘텐츠
  - section : 문서의 일반적인 구분, 컨텐츠의 그룹을 표현
  - article : 문서, 페이지, 사이트 안에서 독립적으로 구분되는 영역
  - footer : 문서 전체나 섹션의 푸터(마지막 부분)
- Non semantic 요소는 div, span 등이 있으며 h1, table 태그들도 시맨틱 태그로 볼 수 있음
- 개발자 및 사용자 뿐만 아니라 검색엔진 등에 의미있는 정보의 그룹을 태그로 표현
- 단순히 구역을 나누는 것 뿐만 아니라 '의미'를 가지는 태그들을 활용하기 위한 노력
- 요소의 이미가 명확해지기 때문에 코드의 가독성을 높이고 유지보수를 쉽게 함
- 검색엔진최적화(SEO)를 위해서 메타태그, 시멘틱 태그 등을 통한 마크업을 효과적을 활용 해야함



### 텍스트 태그

```
<a></a> : href 속성을 활용하여 다른 URL로 연결하는 하이퍼링크 생성
<b></b> : 굵은 글씨 요소
<storng></strong> : 중요한 강조하고자 하는 요소(보통 굵은 글씨로 표현)
<i></i> : 기울임 글씨 요소
<em></em> : 중요한 강조하고자 하는 요소 (보통 기울임 글씨로 표현)
<br> : 텍스트 내에 줄 바꿈 생성
<img> : src 속성을 활용하여 이미지 표현
<span></span> 의미 없는 인라인 컨테이너
```



### 그룹 컨텐츠

```
<p></p> : 하나의 문단(paragraph)
<hr> : 문단 레벨 요소에서 주제의 분리를 의미하며 수평선으로 표현됨
<pre></pre> : HTML에 작성한 내용을 그대로 표현. 보통 고정폭 글꼴이 사용되고 공백문자를 유지
<blockquote></blockquote> : 텍스트가 긴 인용문, 주로 들여쓰기를 한 것으로 표현됨
<div></div> 의미 없는 블록 레벨 컨테이너
```



### 목록 태그

```
<ol> Ordered List
    순서가 있는 목록을 표현할 때 사용한다. type속성으로 글머리 기호를 변경할 수 있다.
<ul> Unordered List
    순서가 없는 목록을 표현할 때 사용한다.
<li> Listed Item
    목록하위 항목으로 사용되며, <ul> 태그 또는 <ol> 태그의 하위에 위치한다.
<dl> Definition List
    Definition List(정의 목록)의 약자로, 사전처럼 용어를 설명하는 목록을 만든다.
    예) A는 B이다. 와 같은 Key = Value로 사용할 때 유용하다.
<dt> Definition Term
    Definition Term(정의 용어)의 약자로, 정의되는 용어의 제목을 넣을 때 사용한다.
<dd> Definition Descripton
    Definition Descripton(정의 설명)의 약자로, 용어를 설명하는데 사용한다.
```

#### 주의사항

- `<dl>`태그는 하나 이상의  `<dt>-<dd>`쌍의 태그를 갖고 있어야 한다.
  - 단, `<dt>-<dd>` 태그가 반드시 하나의 짝으로 지어져야 하는 것은 아니다.
- `li`, `<dt>-<dd>`태그는 밖에서 독립적으로 사용할 수 없다.
- `<ul>` 태그 하위요소로는 `<li>`태그가 위치해야 한다.



### 이미지 태그

`<img>` 태그는 HTML문서에 이미지를 넣는다.

`<img src="images/logo.jpg" alt=logo>`

#### 속성

- src : 필수이며, 이미지로의 경로를 지정한다.
- alt : 이미지의 텍스트 설명이며 필수는 아니지만, 스크린 리더가 `alt`의 값을 읽어 사용자에게 이미지를 설명하므로, 웹 접근성 차원에서 매우 유용하다. 또한 네트워크 오류, 컨텐츠 차단, 죽은 링크 등 이미지를 표시할 수 없는 경우에도 이 속성의 값을 대신 보여준다.
- height : 픽셀 단위의 이미지 고유 크기. 단위 없는 정수여야 한다.
- width : 이미지의 픽셀 기준 고유 너비. 단위 없는 정수여야 한다.

##### 절대경로 vs 상대경로

###### 절대경로

리소스(이미지)의 절대경로는 말 그대로 절대적인 고유한 경로를 지정하는 것이다.

- 웹 이미지 절대경로 [ex) http://www.naver.com/apple.png]
  - http 프로토콜로 시작해서 전체 경로를 입력함
- 웹 이미지 절대경로 [ex) /apple.png]
  - 루트('/') 디렉터리 부터 시작하는 경우 현재 도메인이 자동으로 앞에 붙음
- PC 컴퓨터 절대경로 [ex) C:\user\desktop\img\apple.png]

그러나 절대경로를 이용하면 웹에서 이미지가 사라지거나 내 컴퓨터에서 만든 파일을 다른 곳으로 옮길 때 해당 절대경로를 다시 수정해야 하는 불편함이 있다. 그래서 작업중일 폴더에 이미지를 옮기고 상대적인 위치를 가리킴으로써 이러한 불편함을 해소할 수 있다.

###### 상대경로

상대경로는 현재 문서를 기준으로 경로를 인식하는 방법니다.

- `index.html`에서 동일한 위치에 있는 apple.png를 가져오는 방법 -> `src="apple.png"` 또는 `src="./apple.png"`
- `index.html`의 상위폴더에 이미지가 있는 경우 -> `src="../apple.png"`
- `index.html`의 하위폴더에 이미지가 있는 경우 -> `src="하위폴더/apple.png"`

### 표 태그

- `<table>` 태그- 표
- `<tr>` 태그 - 행
- `<td>` 태그 - 열

#### Table 기본 태그 

- `table` 표를 만드는 태그로써, 표 전체를 감싸는데 사용한다.
- `<caption>` 표의 제목이나 설명을 작성하는 태그
- `<tr>` 표의 행을 의미하는 태그. 자식으로 `<tr>`태그나 `<td>`태그가 반드시 있어야 한다.
- `<th>` 표의 **제목 열**을 의미하는 태그. 부모 태그인 `<tr>`태그 안에 있어야 한다.
- `<td>` 표의 **일반 열**을 의미하는 태그. 부모인 `<tr>`태그 안에 있어야 한다.

#### Table 그룹 관련 태그

- `<colgroup>` 열을 그룹으로 묶을 수 있도록 해주는 태그이다.
- `<col>`: `<colgroup>` 태그의 자식으로 열 단위를 나눌 수 있다. `<span>` 속성을 사용하여 열을 그룹으로 묶을지 설정한다. 예) `<col span="3"> -> 세 개의 열을 그룹으로 묶음`
- `<thead>` : 표의 제목 열들을 묶는 그룹 태그
- `<tbody>`:  표의 일반적인 데이터들을 묶는 그룹태그
- `<tfoot>`: 표의 하단 영역을 묶는 그룹태그

#### Table 태그 관련 속성

- `<th>, <td>`
  - colspan - 열을 병합하는 속성 (가로로 병합한다.)
  - rowspan - 행을 병합하는 속성 (세로로 병합한다.)



# CSS

###### css란?

- 스타일을 지정하기 위한 언어.
- 선택자를 통해 스타일을 지정할 HTML 요소를 선택한다.
- 중괄호 안에서 속성과 값, 하나의 쌍으로 이루어진 선언을 진행한다.
- 각 쌍은 선택한 요소의 속성, 속성에 부여할 값을 의미한다.
  - 속성 (Property) : 어떤 스타일 기능을 변경할지 결정
  - 값 (Value) : 어떻게 스타일 기능을 변경할지 결정
- 모든 요소는 네모(박스모델)이고, 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다.(좌측 상단에 배치)



선택자(Selector), 선언(Decalaration), 속성(Property), 값(Value)

###### CSS 정의 방법

- 인라인 : 해당 태그에 직접 style 속성을 활용한다.
  - `<h1 style="color: blue; font-size: 100px;">Hello</h1>`
- 내부참조( `<style>` )
  - `<head>` 태그 내에 `<style>` 에 지정한다.
- 외부참조(분리된 CSS파일)



### CSS 단위

절대길이단위

![absolute_length](https://user-images.githubusercontent.com/97648339/153757068-5898df0a-e7db-4c39-a798-92d02564d4ec.JPG)

상대길이단위

![relative_length](https://user-images.githubusercontent.com/97648339/153757060-964bfb0a-087e-4f3e-b707-05a77b836200.JPG)

root의 기본 글꼴 크기는 16px이다.



### CSS 색상 단위

- 색상 키워드
  - 대소문자를 구분하지 않음
  - red, blue, black과 같은 특정 색을 직접 글자로 나타냄
- RGB 색상
  - 16진수 표기법 혹은 함수형 표기법을 사용해서 특정 색을 표현하는 방식
    - '#' + 16진수 표기법
    - rgb() 함수형 표기법
- HSL 색상
  - 색상, 채도, 명도를 통해 특정 색을 표현하는 방식
- a는 alpha(투명도)
  - rgba 혹은 hsla 와 같은 형식으로 사용한다.



### CSS 선택자 정리

- 요소 선택자
  - HTML 태그를 직접 선택
- 클래스(class) 선택자
  - 마침표(.)문자로 시작하며, 해당 클래스가 적용된 항목을 선택
- 아이디(id) 선택자
  - #문자로 시작하며, 해당 아이디가 적용된 항목을 선택
  - 일반적으로 하나의 문서에 1번만 사용. 여러번 사용해도 동작하지만, 단일 id를 사용하는 것을 권장

### CSS 적용 우선순위

- 1. 중요도(Importance) - 사용시 주의. 핵폭탄을 투하 하는 격
     - !important
  2. 우선 순위 (Specificity)
     - 인라인 > id > class, 속성, pseudo-class > 요소, pseudo-element
  3. CSS 파일 로딩 순서

- 클래스를 같이 지정했을때는 나중에 선언한 CSS를 따른다.

- ```
  <p class="blue green">3</p>
  <p class="green blue">4</p>가 있을 때
  같은 스타일 시트 내에서
  ```

  ```html
  .green {
  	coloer: green;
  }
  .blue {
  	color : blue;
  }
  ```

  ```
  두 CSS를 정의 했다면 뒤쪽에 선언한 blue CSS를 따른다.
  ```

#### CSS 상속

Text 요소 제외하고는 상속이 되지 않는다고 이해하면 편하다.

- 자손 결합자 `div span`
  - selector A 하위의 모든 selectorB 요소
- 자식 결합자 `div > span`
  - selectorA 바로 아래의 selectorB 요소
- 일반 형제 결합자 `p ~ span`
  - selectorA의 형제 요소 중 뒤에 위치하는 selectorB 요소를 모두 선택
- 인접 형제 결합자 `p + span`
  - selectorA의 형제 요소 중 바로 뒤에 위치하는 selectorB 요소를 선택

### Box model

모든 요소는 네모(박스모델)이고, 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다. (좌측 상단에 배치)

모든 HTML 요소는 box 형태로 되어있다.

하나의 박스는 네 부분(영역)으로 이루어짐

- content : 글이나 이미지 등 요소의 실제 내용
- padding : 테두리 안쪽의 내부 여백. 요소에 적용된 배경색, 이미지는 padding까지 적용
- border : 테두리 영역
- margin : 테두리 바깥의 외부 여백. 배경색을 지정할 수 없다.

#### Box model 구성 (margin/padding)

###### shorthand

margin, padding 값을 정의할때 1개는 모든 면, 2개는 [(상하),(좌우)]를 묶어서, 3개는 [상, (좌우), 하] 순서 4개는 시계방향 [상, 우, 하, 좌]의 순서로 정의한다.

##### box sizing

기본이 content box로 되어있기 때문에 border 까지 정의하기 위해서는 box-sizing을 해줘야 한다.

- box-sizing을 border-box로 설정.

### CSS Display

##### 블록 레벨, 인라인 레벨 요소

###### Block Element

블록 레벨 요소는 부모 요소의 **전체 공간**을 차지하여 "블록"을 만든다. `div` `form` `hr` `<h1>~<h6>` `<ol>` `<ul>` `<li> ` `<p>` 태그 등이 블록 요소에 속한다.

- 화면 구성이나 레이아웃을 짤 때는 블록 레벨 요소를 사용한다.
- 블록 레벨 요소는 한칸을 모두 차지하기 때문에 세로로 나열 된다.
- width, height, margin 속성이 적용된다.
- 콘텐츠 너비가 부족한 부분에 대해서는 자동으로 margin이 부여된다.

###### Inline Element

인라인 레벨 요소는 콘텐츠의 흐름을 끊지 않고(줄바꿈X), 요소를 구성하는 **태그에 할당된 공간만 차지**한다. `<a>` `input, label` `<img>` `<span>` `b, em, i, strong`태그 등이 인라인 요소에 속한다.

- 인라인 레벨 요소는 콘텐츠 영역 만큼 차지하기 때문에 가로로 나열된다.
- margin-top, margin-bottom이 적용되지 않는다. 대신 line-height를 이용
- width, height 속성이 적용되지 않는다. (img 제외)
- 태그가 콘텐츠의 할당된 공간만 갖고 있기 때문에 text-align과 같은 속성을 사용할 수 없다.



###### display: inline-block

- block과 inline 레벨 요소의 특징을 모두 가짐
- inline처럼 한 줄에 표시 가능하고, block처럼 width, height, margin 속성을 모두 지정할 수 있음.

###### display none vs visibility hidden

display none은 아예 콘텐츠를 없애고 visibility hidden 은 눈가리기만 하는 것. 즉, 자리를 차지한다.



### CSS Position

- 문서 상에서 요소 위치를 지정
- static : 모든 태그의 기본 값(기준 위치)
  - 일반적인 요소의 배치 순서에 따른다. (좌측 상단)
  - 부모 요소 내에서 배치될 때는 부모 요소의 위치를 기준으로 배치 됨
- 좌표 프로퍼티 (top, bottom, left, right)를 사용하여 이동 가능한 것
  - relative : 상대 위치
    - 자기 자신의 static 위치를 기준으로 이동한다 (normal flow 유지)
    - 레이아웃에서 요소가 차지하는 공간은 static일 때와 같음 (normal position 대비 offset)
    - 요소가 차지하는 공간은 그대로이기 때문에 위치 변화 시 다음블록 요소가 변화하지 않는다.
  - absolute : 절대 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음(normal flow에서 벗어남)
    - 레이아웃에서 공간을 차지하지 않으므로 다음블록 요소가 좌측 상단으로 붙는다.
    - static이 아닌 가장 가까이 있는 부모/조상 요소를 기준으로 이동 (없는 경우 body)
  - fixed : 고정 위치
    - 요소를 일반적인 문서 흐름에서 제거 후 레이아웃에 공간을 차지하지 않음 (normal flow에서 벗어남)
    - 부모 요소와 관계없이 viewport를 기준으로 이동
      - 스크롤 시에도 항상 같은 곳에 위치함

## Float

- 박스를 왼쪽 혹은 오른쪽으로 배치하여 텍스트 및 인라인 요소가 그 주위를 wrapping 하도록 함
- 요소가 Normal flow를 벗어나도록 함

### Float 속성

- none : 기본값
- left : 요소를 왼쪽으로 띄움
- right : 요소를 오른쪽으로 띄움



# CSS Flexible Box Layout

- 행과 열 형태로 아이템들을 배치하는 1차원 레이아웃 모델
- 축
  - main axis (메인 축)
  - cross axis(교차 축)
- 구성 요소
  - Flex Container (부모 요소)
  - Flex Item (자식 요소)

### Flexbox 축

- flex-direction : row -> main axis가 횡(가로)이 된다.
- 반대로 flex-direction : column -> main axis가 열(세로)이 된다.

### Flexbox 구성 요소

- Flex Container(부모요소)

  - flexbox 레이아웃을 형성하는 가장 기본적인 모델

  - Flex Item들이 놓여있는 영역

  - display 속성을 flex 혹은 inline-flex로 지정

    ```html
    .flex-container {
    	display: fels;
    }
    ```

- Flex Item (자식 요소)

  - 컨테이너에 속해 있는 컨텐츠

----------------

이전까지 Normal Flow를 벗어나는 수단은 Float 혹은 Position이었다.

이때문에 수직정렬이 하기 어려웠고 아이템의 너비와 높이 혹은 간격을 동일하게 배치하기가 어려웠다.

이것을 해결하기 위해 등장한 것이 Flexbox이다.

### Flex 속성 : flex-direction (03_01_flex.html 참조)

- Main axis 기준 방향 설정
  - row (좌->우)
  - row-reverse (우->좌)
  - column (상->하)
  - column-reverse (하->상)

- 역방향의 경우 HTML 태그 선언 순서와 시각적으로 다르니 유의해야한다. (웹 접근성에 영향을 준다.)

### Flex 속성 : flex-wrap

- 아이템이 컨테이너를 벗어나는 경우 해당 영역 내에 배치되도록 설정
- 즉, 기본적으로 컨테이너 영역을 벗어나지 않도록 함
  - wrap
  - nowrap

### flex-flow

- flex-direction과 flex-wrap의 shrorthand
- flex-direction과 flex-wrap에 대한 설정 값을 차례로 작성
- 예시) flex-flow: row nowrap;

### Flex 속성 : justify-content

- 메인 축을 기준으로 배치한다.

### align-content

- cross 축을 기준으로 배치한다.

### align-self

- 개별 아이템을 Cross axis 기준으로 정렬
  - 주의. 해당 속성은 컨테이너에 적용하는 것이 아니라 개별 아이템에 적용한다.

#### 기타 속성

- flex-grow : 남은 영역을 아이템에 분배
- order : 배치 순서 (order를 내리지 않은 item이 맨 앞, 그 뒤 순서대로 들어간다.)





# Bootstrap

css 파일 불러오기 

`<link rel="stylesheet" href="bootstrap.css">`

##### CDN (Content Delivery(Distribution) Network

- 컨텐츠(CSS, JS, Image, Text 등)을 효율적으로 전달하기 위해 여러 노드에 가진 네트워크에 데이터를 제공하는 시스템.
  - 개별 end-user의 가까운 서버를 통해 빠르게 전달 가능(지리적 이점)
  - 외부 서버를 활용함으로써 본인 서버의 부하가 적어짐

##### spacing

| class name | rem  | px   |
| ---------- | :--- | ---- |
| m-1        | 0.25 | 4    |
| m-2        | 0.5  | 8    |
| m-3        | 1    | 16   |
| m-4        | 1.5  | 24   |
| m-5        | 3    | 48   |

| m    | margin  |
| ---- | ------- |
| p    | padding |

### Grid system (web design)

- 요소들의 디자인과 배치에 도움을 주는 시스템
- 기본 요소
  - Column : 실제 컨텐츠를 포함하는 부분, 12컬럼 grid를 기본으로 사용한다.
  - Gutter : 칼럼과 칼럼 사이의 공간 (사이 간격)
  - Container : Column들을 담고 있는 공간
- Bootstrap Grid system은 flexbox로 제작되었다.
- container, rows, column으로 컨텐츠를 배치하고 정렬
- 반드시 기억해야 할 2가지
  - 12개의 column
  - 6개의 grid breakpoints
- 12가 넘어가면 다음 줄로 넘어간다.
  - col-9, col-4, col-3이 있으면 col-9 다음줄에 col-4, col-3이 배치된다.

#### BreakPoint

![grid_breakpoint](https://user-images.githubusercontent.com/97648339/153756929-862a68e6-3553-4066-ac20-fa307a9e5418.JPG)

flex 에도 breakpoint를 사용할 수 있다.



##### nesting

grid 안에 gird를 넣을 수도 있다.

```html
<div class="container">
  <div class="row">
    <div class="col-sm-3">
      Level 1: .col-sm-3
    </div>
    <div class="col-sm-9">
      <div class="row">
        <div class="col-8 col-sm-6">
          Level 2: .col-8 .col-sm-6
        </div>
        <div class="col-4 col-sm-6">
          Level 2: .col-4 .col-sm-6
        </div>
      </div>
    </div>
  </div>
</div>
```

##### offset

grid를 띄우고 싶을 때 사용

마찬가지로 breakpoint를 쓸 수 있다.