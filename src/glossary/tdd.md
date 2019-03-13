# 什么是 TDD
TDD 是测试驱动开发（Test-Driven Development），它同样也是敏捷开发的一种方法论。TDD 是再开发代码之前，先编写单元测试用例，用测试的代码确定要编写什么样的代码。它的整个思路就是通过测试来驱动整个软件开发的进度，当然这对测试人员来说是一个更高的要求和标准。

TDD 三大原则：

* You are not allowed to write any production code unless it is to make a failing unit test pass.
* You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
* You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

翻译：

* 除非要进行失败的单元测试通过，否则不允许编写任何生产代码
* 在一个单元测试中，只允许编写刚好能够导致失败的内容（编译错误也算失败）
* 只允许编写刚好能够使一个失败的单元测试通过的产品代码

TDD 需要大量的实践，并且对参与人员的素质要求相当高，在现在互联网公司中这样的方式还算是比较少的，或许在这种快节奏的变化多端的巨型互联网产品中，项目更加注重商业和流程。当然如果是小而精尖的团队可以考虑这样的模式。