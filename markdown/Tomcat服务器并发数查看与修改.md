## 1. 问题描述

用户访问某张报表时，服务器就使用一个线程来处理报表运算。

如果访问的人数太多且报表运算量大的话，同一时间争抢服务器cpu线程的人就会很多。服务器响应能力就会减弱，所以我们需要合理控制服务器线程个数。

## 2. 解决方法

2.1 设置方式

我们可以通过修改Tomcat服务器的配置，来控制线程数。

打开%Tomcat_HOME%/conf/server.xml文档，找到<Connector port="8080"....>一栏。

在Connector port = "8080"后面加上相应地参数控制线程数，控制参数如下：

| 参数   | 含义   | 默认值  |
|   maxThreads |   tomcat起动的最大线程数，即同时处理的任务个数 |  200 |
|   acceptCount |   当tomcat起动的线程数达到最大时，接受排队的请求个数 |  100 |

要调整Tomcat的默认最大连接数，可以增加这两个属性的值，并且使acceptCount大于等于maxThreads，设置完成后如下：

```xml
   <Connector port="8080" protocol="HTTP/1.1"   
  connectionTimeout="20000"   
  redirectPort="8443" acceptCount="500" maxThreads="400" /> 
```

2.2 注意事项

web server允许的最大连接数还受制于操作系统的内核参数设置，通常Windows是2000个左右，Linux是1000个左右。

这里的连接数是无法直接给出最佳配置的，需要根据您的实际情况，在不断调整，不断测试的基础上，才能达到最合理配置。

转载：http://help.finereport.com/