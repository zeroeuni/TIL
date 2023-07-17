# Typescript
가뭘까 뭐까? typescript 타입스크립트는 자바스크립트의 슈퍼셋인 오픈소스 프로그래밍 언어로 음 쉽게말해 js
업그레이드 버전^^<br>
오류도 잘 찾아주고 더 명확하게 말해줘서 사용하기에 좋다 굿굿이다 완전요물임 ㅎㅎ<br><br><br>

## Import Export
<br>Import -> 쉽게 말해 무언 갈 가져오는 것..
<br>Export -> 쉽게 말해 무언 갈 내보내는 것.. <br><br>

##TYPE 
```ts
- boolean // true, false
- number  // 실수, 정수
- string  // 문자
- object  // 객체
- array   // 배열
- tuple   // 튜플
- enum    // 열거형
- any     // 아무 타입이나 다 들어갈 수 있음 -> 선배님이 쓰면 주겨버린다고하셨다. 쓰면 안좋다. 
- void    // 리턴이 없는 함수
- null    // null
- undefined //undefined
- never   // 불가능을 명시
```
<br><br> 그렇다면 진지하게 왜 any는 쓸 수 없는 것일까.
<br>any를 쓰면 ts를 사용하는 이유가 사라진다!!!!!! 그럴꺼면 js 쓰지 ㅋ ㅎㅎ<br><br><br>

## 타입 주석 
<br>말 그대로 변수 객체 함수 등에 타입을 직접 명시 해 줄 수 있다.
<br>
```ts
const a: number = 10
```
이렇게^^<br><br><br>

## 타입 추론
타입스크립트가 코드를 일겅나가면서 타입을 유추해 내는 것!!!! 타입을 명시하지 않은 상황에서 값을 정해주거나 지정 됐을 때 이루어 진다.
<br>
```ts
const a = 10 // 타입스크립트는 a의 타입을 number로 인식한다.
```

어렵고 머리가 터질 것 같다고?? 그럼 일단 이쯤에서 멈칫..
