#### 찐찐찐막 fuction 과 화살표 함수
<br>

```javascript
function Black() {
  this.name = '흰둥이';
  return {
    name: '검둥이',
    bark: function() {
      console.log(this.name + ' : 멍멍!');
    }
  }
}

const blackDog = new BlackDog();
blackDog.bark.bark(); // 검둥이 멍멍!
```
<br>

```javascript
function WhiteDog() {
  this.name = '흰둥이';
  return {
    name: '검둥이',
    bark : () => {
      console.log(this.name + ' : 멍멍!');
    }
  }
}

const whiteDog = new WhiteDog();
whiteDog.bark(); // 흰둥이 멍멍!
```

<br>
function() 을 사용했을 때는 검둥이가 나타나고, () => 를 사용했을 때는 흰둥이가 나타난다. 
<br> 일반 함수는 자신이 종속된 객체를 this로 가리키며, 화살표함수는 자신이 종속된 인스턴스를 가리킨다.
