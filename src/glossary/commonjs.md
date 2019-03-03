# 什么是 CommonJs
CommonJs 是一种 JavaScript 语言的模块化规范，它通常会在服务端的 Nodejs 上使用。项目是由多个模块组成的，模块和模块之间的调用，需要各个模块有相同规范的 API，这样一来在使用的过程中不会有那么多的学习成本。

在 CommonJs 的模块化规范中，每一个文件就是一个模块，拥有自己独立的作用域，变量，以及方法等，对其他的模块都不可见。CommonJS规范规定，每个模块内部，module 变量代表当前模块。这个变量是一个对象，它的 exports 属性（module.exports）是对外的接口。加载某个模块，其实是加载该模块的 module.exports 属性。require 方法用于加载模块。

```
//modle-a.js
moudle.exports = {
    a: 1
};

//modle-b.js
var ma = require('./modle-a');
var b = ma.a + 2;
module.exports ={
    b: b
};
```
