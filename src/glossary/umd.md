# 什么是【UMD】
UMD 叫做通用模块定义规范（Universal Module Definition）。也是随着大前端的趋势所诞生，它可以通过运行时或者编译时让同一个代码模块在使用 CommonJs、CMD 甚至是 AMD 的项目中运行。未来同一个 JavaScript 包运行在浏览器端、服务区端甚至是 APP 端都只需要遵守同一个写法就行了。

它没有自己专有的规范，是集结了 CommonJs、CMD、AMD 的规范于一身，我们看看它的具体实现：

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

不难发现，它在定义模块的时候回检测当前使用环境和模块的定义方式，将各种模块化定义方式转化为同样一种写法。它的出现也是前端技术发展的产物，前端在实现跨平台的道路上不断的前进，UMD 规范将浏览器端、服务器端甚至是 APP 端都大统一了，当然它或许不是未来最好的模块化方式，未来在 ES6+、TypeScript、Dart 这些拥有高级语法的语言回代替这些方案。

建议阅读，这样对模块化规范的历史道路更加了解：
* 什么是 [CommonJs](./commonjs.md)
* 什么是 [CMD](./cmd.md)
* 什么是 [AMD](./amd.md)