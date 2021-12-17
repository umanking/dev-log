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





