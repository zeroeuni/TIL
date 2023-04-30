<h1>variable이란?</h1>

<p>const → 상수( const a = 5; )값을 바꿀 수 없음</p>
 <p>let →   바꿀 수 있는 변수(let a = 3;) 한번 지정해 두면 나중에 a=4로 바꿀 수 있음.</p>
<br>console.log()는 괄호 안의 내용을 console창에 띄워 주는 것
<br><br>

<h2>데이터 타입</h2>

숫자 , string, bolean(false),null,undefined 등등...
boolean → true, false (amIfat = false;) 

null ‘아무것도 없음’ 0,false와는 다름.<br><br>

<h2>데이터 정리하는 법</h2>
array(배열)

- const dayOfWeek = [”mon”,”tue”,”wed”,”thu”,”fri”,”sat”,”sun”]

오늘은 일요일, 일요일은 항목 7번 이므로

=console.log(dayOfWeek[7]); 로 표현

daysOfWeek.push() → 배열에 원하는 것을 추가하는 방법.

<h2>object 만들기</h2>
선수관련 object를 만들어 보자.<br>
const player = {

name: “youngeun”,

points: 20,

fat: false,

**};**
[player.name](http://player.name) (player.name 이라는 object를 만든 것.)

=console.log(player[”name”])과 결과가 같음

object를 업데이트 할 수도 있음

player.points = 30; (현재의 points에 30을 더하고싶다면?  —> player.points = player.points+30; 의 형식으로 나타내기)

object를 추가할 수도 있음

player.lastName = “potato”; 없던 lastname을 추가한 거임.


