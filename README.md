# boot从0到一 我的项目名称是boot-back
来自掘金的springboot博客系列 https://juejin.im/user/59e7fb9451882578e1406a51/posts
1、搭建简单的SpringBoot项目，完成MVC开发，实现从前台请求到后台数据库查询的三层架构的流程。
2、引入druid数据库连接池，实现监控功能。
3、将请求结果封装成统一格式。
4、添加自定义消息转换器，这个有什么作用呢？
场景分析：后台接口返回一个实例，当你需要使用某个属性的值时，你还要判断一下值是否为null；接口返回一堆属性值为null的属性等
分析：消息转换器可以帮你解决这个问题。添加fastjson依赖
5、添加全局异常处理
为什么要这样做呢？
在互联网时代，我们所开发的应用大多是直面用户的，程序中的任何一点小疏忽都可能导致用户的流失，而程序出现异常往往又是不可避免的，所以我们需要对异常进行捕获，然后给予相应的处理，来减少程序异常对用户体验的影响
6、添加Swagger2来在线自动生成接口的文档+测试功能
Swagger是一款通过我们添加的注解来对方法进行说明，来自动生成项目的在线api接口文档的web服务。
7、添加PageHelper分页查询功能，PageHelper是一款好用的开源免费的Mybatis第三方物理分页插件
物理分页支持常见的 12 种数据库。Oracle,MySql,MariaDB,SQLite,DB2,PostgreSQL,SqlServer 等
支持多种分页方式支持常见的RowBounds(PageRowBounds)，PageHelper.startPage 方法调用，Mapper 接口参数调用
需要添加jar包依赖
启动时报错，经过查询原来是jar包版本的问题。
org.springframework.beans.factory.BeanCreationException: Error creating bean with name 'com.github.pagehelper.autoconfigure.PageHelperAutoConfiguration': Post-processing of merged bean definition failed; nested exception is java.lang.IllegalStateException: Failed to introspect Class [com.github.pagehelper.autoconfigure.PageHelperAutoConfiguration] from ClassLoader [sun.misc.Launcher$AppClassLoader@2a139a55]
将PageHelper升级为1.2.5版本，即可解决。（原来版本是1.1.2）
8、集成通用 Mapper功能
通用 Mapper 是一个可以实现任意 MyBatis 通用方法的框架，项目提供了常规的增删改查操作以及Example 相关的单表操作。
通用 Mapper 是为了解决 MyBatis 使用中 90% 的基本操作，使用它可以很方便的进行开发，可以节省开发人员大量的时间。
此时，将主键类型由Integer类型改为varchar类型，主键生成策略由框架来实现。实现发号器。
9、集成generator自动生成model，xml，dao功能
10、
