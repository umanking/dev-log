## 1. 노드 시작하기

```js
function run(){
    console.log('3초후 실행'); 
}
console.log('시작');
setTimeout(run, 3000); 
console.log('끝');
```

- 이벤트 루프
- 백그라운드
- 테스크큐

1. 호출스택에 setTimeout이 쌓임
2. setTimeout실행시 콜백run은 백그라운드로 보내짐
3. 백그라운드에서 3초후에 테스크 큐로 보내짐
4. 이벤트 루프가 돌면서 큐에있는걸 호출스택으로 올림
5. run이 호출스택에서 비워지고, 이벤트 루프는 큐에 콜백이 들어올때까지 대기





## 2. 알아두어야할 자바스크립트

- const, let은 블록스코프를 가짐 (그에 반해 var는 함수 스코프를 가짐) -> 그렇기 때문에 호이스팅 문제를 해결함
- 기본적으로 const를 사용하자





## 3. 노드 기능알아보기 

1. REPL 사용하기 
2. js파일 실행하기 
   1. `node helloworld`  (helloworld.js파일 실행)
3. 모듈로 만들기 
   1. import, export default (ES2015모듈)
4. 노드 내장객체 알아보기 
   1. global