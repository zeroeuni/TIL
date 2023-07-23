# Promise와 Async/Await에 대해!
Promise와 async/await는 비동기 코드를 다룰 때 유용한 패턴들로서, 타입스크립트에서도 지원.</br> 이들을 자세히 설명해보자!
</br>

## Promise
Promise는 비동기 작업의 결과를 나타내는 객체이다. </br> 비동기 작업은 주로 네트워크 요청, 파일 읽기, 데이터베이스 쿼리 등과 같이 시간이 걸리는 작업을 말한다.</br> Promise는 성공(resolve) 또는 실패(reject) 두 가지 상태를 가질 수 있다.</br>
```TypeScript
const fPromise: Promise<ReturnType> = new Promise((resolve, reject) => {
  // 비동기 작업 수행
  // 성공적으로 작업을 완료하면 resolve(value)를 호출하여 결과를 반환
  // 작업이 실패하면 reject(error)를 호출하여 오류를 반환
});
```
</br>

## Promise 어떻게 사용하나요
Promise를 사용할 때는 then과 catch 메서드를 이용하여 비동기 작업의 성공과 실패를 처리할 수 있다. </br>또한, ES8(ES2017)부터 도입된 async/await 구문을 사용하여 보다 편리하게 처리할 수 있다.</br>

1: then/catch를 이용한 Promise 사용
```typescript
function fetchData(): Promise<string> {
  return new Promise((resolve, reject) => {
    // 비동기 작업을 시뮬레이션하는 setTimeout
    setTimeout(() => {
      const data = "Data from the server";
      if (data) {
        resolve(data); // 성공적으로 작업이 끝났을 때
      } else {
        reject(new Error("Failed to fetch data")); // 작업이 실패했을 때
      }
    }, 2000);
  });
}

// Promise 사용
fetchData()
  .then((data) => {
    console.log(data); // "Data from the server"
  })
  .catch((error) => {
    console.error(error); // Error: Failed to fetch data
  });
```
</br>

## Async/Await
async/await는 Promise를 더 편리하게 다룰 수 있도록 도와주는 구문이다.</br> async 함수 안에서 비동기 작업을 동기적으로 처리할 수 있게 해준다.</br>

async/await의 구조
async 함수 내부에서 await 키워드를 사용하여 Promise를 기다릴 수 있다.</br> await 키워드는 Promise가 성공(resolve)할 때까지 기다리고, 결과를 반환한다.</br> 만약 Promise가 실패(reject)하면, 오류를 throw하게 된다.</br>

```typescript
async function myAsyncFunction(): ReturnType {
  // 비동기 작업을 수행하고 결과를 반환하는 로직
  const result = await someAsyncOperation();
  return result;
}
```

## Async/Await 사용하기
2: async/await를 이용한 Promise 사용</br>
```typescript
// 위의 fetchData 함수를 async/await로 사용하기
async function fetchData(): Promise<string> {
  return new Promise((resolve, reject) => {
    // 비동기 작업을 시뮬레이션하는 setTimeout
    setTimeout(() => {
      const data = "Data from the server";
      if (data) {
        resolve(data); // 성공적으로 작업이 끝났을 때
      } else {
        reject(new Error("Failed to fetch data")); // 작업이 실패했을 때
      }
    }, 2000);
  });
}

// async/await 사용
async function getData() {
  try {
    const data = await fetchData();
    console.log(data); // "Data from the server"
  } catch (error) {
    console.error(error); // Error: Failed to fetch data
  }
}

getData();
```
</br>
async/await를 사용하면 Promise의 then/catch를 사용하는 것보다 코드가 간결하고 가독성이 좋아진다.</br> async 함수 내에서는 동기적인 코드처럼 보이면서도 비동기 작업을 처리할 수 있다.</br>

아직 이론에 대해서만 알고 직접 해보지 않아서 딱 와닿고 이해되는 느낌은 없지만,</br>
흐름을 이해했으니 내일은 이를 직접 실행해보도록 하자!!
