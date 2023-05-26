<h1>react에서의 import와 export에 대해 알아봅시당.</h1>  
<h2>import - 가져오기</h2>  
  
  
리액트에서 코드가 점점 많아지면 하나의 파일에 작성하기 어려워지는데,  

이러한 문제를 해결하기 위해 자바스크립트에서는 모듈(module)이라는 기능을 지원하여 하나의 파일을 여러개의 파일로 나눌 수 있도록 해놨다!!!!  
  
  
즉 파일을 분리해서 사용할 수 있다!  
  
  
<b>App.js 파일과 List.js 두개를 연결 해 보자!</b>  

```App.js
import List from './List.js';  
```     
    
    
    
    
  
  이렇게 App.js에서 List.js파일의 내용을 가져와서 사용할 수 있다.  
    
    
    
    
<h2> export - 내보내기</h2>  

변수, 함수, 클래스 앞에 export 키워드를 붙여서 모듈의 기능을 외부에서 사용할 수 있도록 내보내는 것.  

import는 그럼 export로 내보낸 모듈을 가져오는 기능을 담당한다.  
```App.js
const App () => {  
};  

export default App;
```

  
