# 什么是【MVP】
MVP 是 Model-View-Presenter 的缩写，它是经典软件设计模式 MVC 演变而来，同样 Model 负责数据；View 负责显示；Presenter 类似于 Controller负责业务逻辑。与 MVC 不同之处在，MVC 的 View 会直接使用 Model，然而 MVP 的 View 不会直接使用 Model，而是通过 Presenter 和 Model 进行通讯，所有的交互都是发生在 Presenter 中。

MVP 的好处就是将 View 和 Model 进一步解耦，主要的程序在 Presenter 中实现；同样我们可以将一个 Presenter 用于多个 View ，达到代码复用的效果；另外借助 View 和 Presenter 的分离，我们可以很容易的对表现层进行单元测试。

MVP 模式在 APP 特别是 Android APP 上运用到比较多，它给我们的开发带了了更多的好处。

〖坚持的一俢〗