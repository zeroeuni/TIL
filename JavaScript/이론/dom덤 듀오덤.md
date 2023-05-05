## html에 js를 접근시키기!
<br><br>
```js
document.getElementById('지정한 아이디 명')//지정한 아이디의 태그가 불러와짐
document.getElementsByClassName('클래스 명')//지정한 클래스의 태그가 불러와짐
document.querySelector('#아이디') 
document.querySelector('.클래스')
```


#### <br><br>카멜케이스로 작성하는게 원칙 (ex. getElementsByClassName)
<br>innerText라는 속성으로 문자를 바꿀 수 있음
<br>addEventListener('click', 함수명) 무언가를 클릭했을 때 '함수명' 실행!!
<br> const li = document.createElement('li')생성과 동시에 변수에 태그를 만들기.
<br>.appendChild('태그') 요소 만들기
<br><br>

```js
del.addEventListener("click", deleteList); //클릭했을 때 deleteList 실행
function deleteList(e){ //삭제 버튼(x) 클릭시 
    let remove1 = e.target.parentElement;  //선택한 목록 한개만 지우기
    remove1.remove();
}
