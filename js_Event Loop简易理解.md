执行机制：Event Loop

js 任务定义：

1. 宏任务macro-task：整体的script、setTimeout、setInterval
2. 微任务micro-task：Promise、process.nextTick

任务执行顺序：

- 宏任务
- 微任务

代码执行顺序可以理解为（一个宏任务 + 一个微任务队列）的循环执行；

一个宏任务对应1个微任务队列

Q：setTimout本意应该是在x秒后，把执行内容插入到Event Queue中，在主程序代码空余时执行。

例：

````javascript
setTimeout(function() {
    console.log('setTimeout');
}, 0);
````

