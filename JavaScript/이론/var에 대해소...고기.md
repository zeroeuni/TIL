var와 let은 거의 비슷하다고 이해했고!!! 거의 똑같다고 생각했는데, 거의 똑같다면 만들어지지 않앗겠지요?<br>
그렇다면 var와 let의 차이점을 알아보좌.
var와 let은 같은 작동을 하는 듯 보이지만 선언 할 때 약간 쓰 다르다는 점

var는 전역 범위 또는 함수 범위이지만!!
let은 블록 범위 이다!!!!  
<br> 
```js
function haha( ) {
    var ha = 13;
    console.log(ha) // 13
}

console.log(ha) // undefined
```
<br>
var로 선언한 변수는 전역변수로 선언이 되지만! 지역변수에서 핸들링한 값은 들어가지 않는당.  

또한 var는 변수 재선언이 가능하지만 let은 재선언 할 수 없다!!
