# 什么是【注入】
注入通常指的是一种攻击方式，它利用系统或者程序语言的漏洞，通过外部（传入参数）对系统进行一种非法的操作。在网站系统中通常有 SQL 注入，JavaScript 脚本注入等方式来破坏系统原有的运行状态。

SQL 注入会通过 SQL 语句，在外部传入一些对数据库的操作语句，对数据库进行破坏，这种破坏是非常厉害的，甚至是可以删除数据库的所有数据，当然现代的语言框架已经解决了这一问题，通过框架会禁止所有的外部非法 SQL 操作。

JavaScript 脚本注入，也是通过传递脚本到网页中，让网站表现层出现异常导致无法使用。当然这种破坏力度有限，通过快速不定上线可以解决这一问题。

通常的注入攻击，现在很多框架已经解决这一问题，我们不用太担心，担心的是在框架的使用上不规范导致的漏洞，一定好做好安全措施。

〖坚持的一俢〗