# 什么是 AMD
AMD 叫做异步模块定义规范（Asynchronous Module Definition），同样它是 [CommonJs](./commonjs.md) 模块化规范的超集，但是运行于浏览器之上的，关于模块化的好处我们在 [CommonJs](./commonjs.md) 篇文章中我们了解过。AMD 的特点就和它的名字一样，模块的加载过程是异步的，它大大的利用了浏览器的并发请求能力，让模块的依赖过程的阻塞变得更少了。requireJs 就是 AMD 模块化规范的实现。

AMD 作为一个规范，只需定义其语法 API，而不关心其实现。AMD 规范简单到只有一个 API，即 define 函数：

```
 define(id?, dependencies?, factory);
```

具体用法如下：

```
// moudle-a.js
define('moudleA', function() { 
    return {
        a: 1
    }
});

// moudle-b.js
define(['moudleA'], function(ma) {
    var b = ma.a + 2;

    return {
        b: b
    }
});
```

它看起来似乎和 CMD 差不多，不过在实现上还是有一定的差异，它们各有差异各有优缺点，我们未来回专门对这些模块化规范做对比。