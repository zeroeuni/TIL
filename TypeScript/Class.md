# Class
클래스(Class)는 객체 지향 프로그래밍의 기본적인 개념 중 하나로,<br>
타입스크립트에서도 자바스크립트와 마찬가지로 클래스를 사용하여 객체를 생성하고 관리할 수 있다.

<br>

```ts
class ClassName {
  // 클래스의 프로퍼티들
  property1: type;
  property2: type;

  // 생성자 메서드 (constructor)
  constructor(param1: type, param2: type) {
    this.property1 = param1;
    this.property2 = param2;
  }

  // 클래스의 메서드들
  method1() {
    // 메서드 동작 정의
  }

  method2() {
    // 메서드 동작 정의
  }
}
```
<br> 
이 클래스를 이용해 자기소개를 해 본다면?
<br>
<br>

```ts
class Information {
  name : string;
  age : number;

  cunstructor(name : string, age : number) {
    this.name = name;
    this.age = age;
}

sayHello{
  console.log(`안녕하세요, 저는 ${this.name}이고 ${this.age}살입니다.`);    
}

const person1 = new Person("Mimi", 30);
const person2 = new Person("Youngeun", 17);

// 메서드 호출
person1.sayHello(); // 출력: 안녕하세요, 저는 Mimi이고 30살입니다.
person2.sayHello();
```
