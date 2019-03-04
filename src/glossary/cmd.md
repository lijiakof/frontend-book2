# 什么是 CMD
CMD 叫做通用模块定义规范（Common Module Definiton），它是类似于 [CommonJs](./commonjs.md) 规范但是运行于浏览器之上的，关于模块化的好处我们在 [CommonJs](./commonjs.md) 篇文章中我们了解过。它是随着前端业务和架构的复杂度越来越高运用而生的，来自淘宝玉伯的 SeaJS 就是它的实现。

CMD 规范尽量保持简单，并与 CommonJS 的 Modules 规范保持了很大的兼容性。通过 CMD 规范书写的模块，可以很容易在 Node.js 中运行。在 CMD 规范中，一个模块就是一个文件。格式如下：

```
define(factory);
```

具体用法如下：

```
// moudle-a.js
define(function(require, exports, module) {

    module.exports = { 
        a: 1 
    };

});

// moudle-b.js
define(function(require, exports, module) {

    var ma = require('./moudle-b');
    var b = ma.a + 2;
    module.exports = { 
        b: b 
    };

});
```

CMD 规范拥有简单、异步加载脚本、友好的调试并且兼容 Nodejs，它的确在开发过程中给我们提供了较好的模块管理方式。