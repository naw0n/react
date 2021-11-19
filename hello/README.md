## REACT 공부
### React 란
사용자 인터페이스를 구축하기 위하 선언적이고 효율적이며 유연한 javascript 라이브러리
컴포넌트를 이용해 복잡한 ui를 구성하도록 돕는다.

1. 웹페이지가 만들어지는 과정
![웹페이지 구성](https://media.vlpt.us/images/juno7803/post/4cce674a-e2b1-4bf3-be04-57891ed90a87/image.png)
html : 기본틀, css : 스타일, javascript : 동적으로 제어
    1. HTML parser 가 HTML을 바탕으로 DOM tree를 그린다.
    2. CSS parser가  CSS를 바탕으로 CSSOM을 그린다.
    3. DOM에 CSSOM을 적용하여, Render Tree 를 그린다.
    4. Render Tree를 바탕을 painting하여 실제 화면에 렌더링 한다.
    * HTML 코드를 읽어 내려가다가 <script></script> 태그를 만나면 파싱을 잠시 중단하고 js 파일을 로드한다.

  - DOM(Documnet Object Model) : html요소의 구조화된 표현, 객체 해당한다.
  웹브라우저와 javascript가 HTML을 이해하기 쉽도록 트리 구조를 파싱하여 만든 객체
  - CSSOM(Cascading Style Sheets Object Model) : DOM에 CSS가 적용된 객체 모델

2. Virtual DOM
DOM을 직접 조작하며 안정성이 떨어질 뿐만 아니라, DOM API가 low-level이기 때문에 조작할수록 코드의 복잡도가 매우 높아진다.
비유 ) tv(DOM) 리모콘(virtual DOM)
사용자가 Virtual DOM을 조작하는건 React와 같은 라이브러리가 비교적 쉽게 해줄 수 있다.

3. React Web App의 Rendering

4. 컴포넌트
```js
import React from 'react';
```
리액트의 여러기능을 사용할 수 있도록 한다.

```js
function 컴포넌트명() { // 컴포넌트 첫 번째 글자는 대문자로 작성한다.
    return (
        반환할 JSX
    );
}
```
개념적으로 컴포넌트는 자바스크립트 함수이다. 
임의의 props 라는 Input 을 받아서 화면에 무엇이 보여질지 기술하는 리액트 엘리먼트를 Output 으로 반환 <br>
컴포넌트 정의 방법 : 함수 또는 클래스로 생성 <br>
컴포넌트의 장점 : 독립적, 재사용 가능

5. JSX : html, javascript를 조합한 문법
- JSX 안에 컴포넌트를 넣을 수 있다.
- HTML태그도 사용
- 여러개의 컴포넌트를 사용하려면 하나의 태그에 감싸야 한다.
```
html과 다르게 class 속성 사용 안함. -> className 속성 사용
html과 다르게 주석 사용시 {/* 내용 */} - vs code 단축키 command + /
html과 다르게 단독태그 허용 x. br, img, input 태그 닫아줘야함.
```

출처 : https://velog.io/@juno7803/React가-태어난-배경
https://www.everdevel.com/ReactJS/
https://velog.io/@ingong/React-Component-와-Props-State-에-대해서-알아보자
