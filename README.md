# NOTE
### a.domain.com,b.domain.com能不能共享cookie?如果不同域如何处理？
相同域名的cookie是可以共享的，不同域的时候可以采用sso单点登录系统的方式

这个系统集中处理用户信息、登录等信息

此时业务站点A，不处理用户的登录信息

服务器端在用户第一次提交请求时，跳转到UserCenter系统验证是否登陆

如未登录，重定向到UserCenter系统的登录页

用户登录成功以后，再回跳到业务站点A原来的页面

这个时候，业务站点A把带回来的用户信息存到session中，之后A站点就一直有户的登录信息了

### 传统布局和flex的区别
css盒子模型不是某种布局专属的，是所有布局共同的。传统布局这个词太泛泛，目前在用的主流方法主要有两类。
- 基于格子布局，将页面看成行+列的二维布局（grid layout）
- flex布局，将页面看成行或者列的一维布局。

到现在这个时代，其他的方法都归为传统布局,比如传说中的默认布局。还有基于float实现多列的布局、依赖table的表格布局。

性能上flex允许子元素不设置宽高，而是由算法动态去计算，性能会比设定好宽高的稍慢。就现在来说没有大影响，但计算有时候会不符合人的预期，有时候需要用flex提供的属性给予启发。

相关问题：

- flex几种历史的写法，比如哪些浏览器支持-webkit-box？
- flex目前是w3c的提议还是标准？
- 什么是布局？flex在移动端兼容性？
- 文档流的概念

https://developer.mozilla.org/zh-CN/docs/Learn/CSS/CSS_layout
