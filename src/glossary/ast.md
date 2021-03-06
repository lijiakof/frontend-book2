# 什么是【AST】
AST （Abstract Syntax Tree）是抽象语法树的英文简称，它从源代码到运行的编译程序过程中起到重要的作用。

AST 是源代码语法结构的一种抽象表现形式，通常以树的数据结构来表达，树上每一个节点都表现出源代码中的结构，我之前在[《【Babel 极速指南】》](https://www.jianshu.com/p/23abbdaa119e) 这篇文章中介绍过 Babel 编译器的编译过程，它将 JavaScript 的高级版本编译成低级版本，整个过程离不开抽象语法树对源代码的抽象过程。

抽象语法树不仅可以做到源代码到二进制程序的过程，也能做到源代码到源代码的过程，很多语言的转换就是通过对两种规则的 AST 做转化，再加上语法的补充来完成。如果想了解编译原理可以好好学习它。

〖坚持的一俢〗