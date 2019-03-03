# 什么是 CommonJs、CMD、AMD、UMD？
CommonJs、CMD、AMD、UMD 这些都是 JavaScript 模块的规范，随着业务复杂度的增加，模块化规范成为大型项目组织的重要规划。当然我们在这里不回去比较它们的好与坏，在这里我们只会对它们到底是什么做个介绍。

## CommonJs
CommonJs 主要运用在服务器端的 JavaScript，Nodejs 就是采用的 CommonJs 的模块化规范：

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

## CMD
CMD 叫做通用模块定义规范（Common Module Definiton），它是类似于 CommonJs 规范但是运行于浏览器之上的，也是随着前端业务和架构的复杂度越来越高运用而生的，SeaJS 就是它的实现。

```
define((require, exports, module) => {
    //todo
});
```

## AMD
AMD 叫做异步木块定义规范（Asynchronous Module Definition），Web 程序在追求模块化的道路中又继续思考，一次性的加载所有 JavaScript 对 Web 程序来说性能上是不够好的，AMD 这种按需的模块加载方式得到一部分前端开发者的推崇，其中著名的 RequireJs 就是这种定义的实现：

```
define(['jquery', 'underscore'], function ($, _) {
    //todo
});
```

## UMD
UMD 叫做通用模块定义规范（Universal Module Definition）。也是随着大前端的趋势所诞生，它可以通过运行时或者编译时让同一个代码模块在使用 CommonJs、CMD 甚至是 AMD 的项目中运行。未来同一个 JavaScript 包运行在浏览器端、服务区端甚至是 APP 端都只需要遵守同一个写法就行了。

```
((root, factory) => {
    if (typeof define === 'function' && define.amd) {
        //AMD
        define(['jquery'], factory);
    } else if (typeof exports === 'object') {
        //CommonJS
        var $ = requie('jquery');
        module.exports = factory($);
    } else {
        root.testModule = factory(root.jQuery);
    }
})(this, ($) => {
    //todo
});
```