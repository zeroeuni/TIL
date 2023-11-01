# for
초깃값부터 시작해서 증가 또는 감소하면서 조건에 부합하면 계속 순회.
중간에 "break;" 문을 만나면 반복문을 중단.

# foreach
배열의 각 요소에 대해 callback을 실행.<br>
배열을 순회하므로 중간에 "break;" 문을 사용할 수 없다. 이런 경우라면 for( )문을 사용해야 함.

# map
배열의 각 요소에 대해 callback을 실행하고 실행결과를 모은 새 배열을 리턴<br>
배열을 순회하므로 중간에 "break;" 문을 사용할 수 없음. 이런 경우라면 for( )문을 사용해야함.

### key
리액트에서 key는 컴포넌트 배열을 렌더링했을 때 어떤 원소에 변동이 있었는지 알아내려고 사용한다.</br>
예를 들어 유동적인 데이터를 다룰 때는 원소를 새로 생성할 수도, 제거할 수도, 수정할 수도 있다.</br>
key가 없을 때는 Virtual Dom을 비교하는 과정에서 리스트를 순차적으로 비교하면서 변화를 감지한다. </br>
하지만 key가 있다면 이 값을 사용해서 어떤 변화가 일어났는지 더욱 빠르게 알아낼 수 있다. 
#### key값을 index로 주게되면 매우 비효율적 (고유한 값이 없을 때만 index사용)