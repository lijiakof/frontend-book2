# 什么是【FHS】
FHS（Filesystem Hierarchy Standard）是文件系统层级标准的英文简称。Liunx 系统的文件组织形式就是采用的这一标准。

它的主要目的是希望让使用者可以了解到已安装软件通常放置于那个目录下，所以他们希望独立的软件开发商、操作系统制作者、以及想要维护系统的使用者，都能够遵循FHS的标准。 也就是说，FHS的重点在于规范每个特定的目录下应该要 放置什么样子的数据而已。

分类维度：

* 可共享的
* 不可共享的
* 不变的
* 可变动的

三层目录定义：

* `/`（root, 根目录）：与开机系统有关；
* `/usr`（unix software resource）：与软件安装/执行有关；
* `/var`（variable）：与系统运行过程有关。

〖坚持的一俢〗