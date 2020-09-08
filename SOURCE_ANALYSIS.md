# 目录结构
``` 
├── catalina    -- Tomcat提供的Servlet容器实现,负责处理来自客户端的请求并输出响应
│   ├── ant    -- 使用ant集成jmx, 方便运行时对Tomcat实例进行管理
│   ├── authenticator    
│   ├── connector    -- 处理连接用的，比如HttpSevletRequest
│   ├── core    -- sevlet核心核心实现
│   ├── deploy    -- 部署模块
│   ├── filters    -- 内置filter实现
│   ├── ha    -- Hight available缩写，处理tomcat集群
│   ├── loader    -- tomcat类加载器
│   ├── manager    -- 
│   ├── mapper
│   ├── mbeans    -- Tomcat内置的jmx
│   ├── realm    -- tomcat管理页面的权限控制
│   ├── security    -- 安全相关
│   ├── servlets    -- servlets 实现类
│   ├── session    -- httpSession相关
│   ├── ssi    -- server side includes(SSI)， 用于替换html片段，类似Nginx处理ssi资源
│   ├── startup    -- 主要用于启动Tomcat容器 
│   ├── storeconfig    -- 配置信息
│   ├── tribes    -- 部落组件，用于tomcat之间通信
│   ├── users
│   ├── util
│   ├── valves
│   └── webresources    -- 用于处理jar、war等文件
├── coyote    -- 中文为狼，用于处理各种协议， Coyote是Tomcat链接器框架的名称,是Tomcat服务器提供的供客户端访问的外部接口,客户端通过Coyote 与Catalina容器进行通信
│   ├── ajp    -- ajp协议
│   ├── http11    -- http1.1协议
│   └── http2    -- http2.0协议
├── el    -- el表达式 (优先级放低)
│   ├── lang
│   ├── parser
│   ├── stream
│   └── util
├── jasper    -- Tomcat的jsp引擎,我们可以在jsp中引入各种标签,在不重启服务器的情况下,检测jsp页面是否有更新,等等,还是上面那句话,现在前后端分离比较多,以后的学习,我们也以关注上面的Catalina和Coyota为主
│   ├── compiler
│   ├── el
│   ├── resources
│   ├── runtime
│   ├── security
│   ├── servlet
│   ├── tagplugins
│   ├── util
│   └── xmlparser
├── juli    -- 日志相关 
│   └── logging
├── naming    -- 
│   ├── factory
│   └── java
└── tomcat    -- 对javax的一些实现
    ├── buildutil
    ├── dbcp    -- 数据库连接池实现
    ├── jni    -- native实现，需要使用tomcat提供的tomcat-native.tar.gz
    ├── util    -- 各种工具类，包括对jdk的封装
    └── websocket    -- 对javax.websocket的实现
```