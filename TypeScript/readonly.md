# Readonly 
타입스크립트에서 readonly 속성은 변수나 속성에 대해 변경을 허용하지 않고 읽기 전용으로 설정하는 기능이다.</br>
즉, readonly로 선언된 변수나 속성은 한 번 값이 할당되면 그 이후에는 수정이 불가능하다.</br>
readonly 속성은 주로 클래스의 속성이나 인터페이스의 속성에 사용되며, 이를 이용하면 코드의 안정성을 높이고, 실수로 값이 변경되는 것을 방지할 수 있다.

## 클래스에서 readonly 사용하기

```typescript
class Person {
  readonly name: string;
  readonly age: number;

  constructor(name: string, age: number) {
    this.name = name;
    this.age = age;
  }

  // readonly 속성은 생성자에서 초기화할 때만 값을 할당할 수 있음
}

const person = new Person("John", 30);
console.log(person.name); // "John"
person.name = "Mike"; ->에러가 뜨게 된다.
```
</br></br>

## 인터페이스에서 readonly 사용하기
```typescript
interface Point {
  readonly x: number;
  readonly y: number;
}

const point: Point = { x: 10, y: 20 };
console.log(point.x); // 10
point.x = 30; // Error
```
</br></br>

ReadonlyArray를 사용하면 배열의 메서드를 통해 변경을 시도하는 것도 방지된다.

```typescript
const arr: ReadonlyArray<number> = [1, 2, 3];
arr.push(4); // Error: Property 'push'
```
</br>
readonly를 사용하면 안정성있는 코드를 작성할 수 있다.
