# Frontend Question

Below are Questions I've been asked during the interview

> What is closure?

Inner function can access outer function's variable and parameters.

provide example

> What is prototype? How do you do inheritance? What is Prototype Chain?

[answer](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)

JS doesn't implement class in its language. ES6 comes with class but its syntactic sugar.

Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.

> Write a class B that inherits class A

```js
function A() {
  this.name = 'A'
}

function B() {
  A.call(this, ...arguments);
}

B.prototype = Object.create(A.prototype);
```

> What is this?

[mdn](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Operators/this)

```
JavaScript 函式內的 this 關鍵字表現，和其他語言相比略有差異。
在嚴格模式與非嚴格模式下也有所不同。

通常，this 值由被呼叫的函式來決定。它不能在執行期間被指派，
每次函式呼叫調用的值也可能不同。ES5 引入了 bind 方法去設置函式的 
this 值，而不管它怎麼被呼叫。ECMAScript 2015 也導入了定義 this 
詞法範圍的箭頭函式（它的 this 值會維持在詞法作用域）。
```

將會改變 this

* new keyword
* bind
* call, apply

> Explain Box Model

> What is the property to set width to equal to width=padding + margin + width

> name all position properties

> name all display properties

> Array splice, pop, unshift, shift, push forEach, reduce, slice

> Rewrite jQuery $('.test').delete() in vanilla js

> What is event delegation? Why do you need it?

> Explain event bubbling and capturing

> What is EventLoop?

> What is difference between block, inline-block and inline

> Margin collapse

> How do you position element in center horizontally and vertically?

> Explain this css

```
a   b {}
a > b {}
a + b {}
a ~ b {}
```