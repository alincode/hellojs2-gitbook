# 非同步 (async)

<!--
1-1 start coding (async)
2 answer customer phone (sync)
3-1 buy drink - call phone (async)
1-2 continue coding (async)
3-2 drink is comming (async)
1-3 finish coding (async)
-->

* 非同步的日常例子
* JavaScript 語言的一大特點就是單執行緒，同一個時間只能做一件事。
* 所有事件可以分為 synchronous 和 asynchronous。
* 同步事件指的是，在主線程上排隊執行的任務，只有前一個任務執行完畢，才能執行後一個任務。
* 非同步事件指的是，先進入 task queue (event loop)，task queue 通知主線程(stack)，若主線程有空該任務才會進入主線程執行。

![](assets/event-loop.png)

* event loop

```js
function now() {
  return 'Hello......';
}

function later() {
 console.log('step2');
  message += 'World';
  console.log(message);
}

console.log('step1');
var message = now();
console.log(message);
setTimeout(later, 5000);
console.log('step3');
```

### 延伸閱讀

<!-- 從 6:40 開始看 -->

* [Philip Roberts: Help, I’m stuck in an event-loop. on Vimeo](https://vimeo.com/96425312)
* [並發模型和事件循環 - JavaScript | MDN](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/EventLoop)