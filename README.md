# boot从0到一 我的项目名称是boot-back
来自掘金的springboot博客系列 https://juejin.im/user/59e7fb9451882578e1406a51/posts
1、搭建简单的SpringBoot项目，完成MVC开发，实现从前台请求到后台数据库查询的三层架构的流程。
2、引入druid数据库连接池，实现监控功能。
3、将请求结果封装成统一格式。
4、添加自定义消息转换器，这个有什么作用呢？
场景分析：后台接口返回一个实例，当你需要使用某个属性的值时，你还要判断一下值是否为null；接口返回一堆属性值为null的属性等
分析：消息转换器可以帮你解决这个问题。添加fastjson依赖
