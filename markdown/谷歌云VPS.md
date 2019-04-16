## 利用谷歌云平台GoogleCloudPlatform搭建vps

### 前提条件

1：拥有一张信用卡，Visa或者MasterCard或者JCB

2：有一个可以临时翻墙的环境，都是脸书的网友想必这个就不必操心了能上脸书的都是已经翻墙的。

3：工具软件，从以下网址下载对应平台的shadowsocks

http://shadowsocks.org/en/download/clients.html

4：拥有谷歌账户

![](http://www.wangcong.online/upload/2019/3/image120190411024405297.jpeg)

### 创建vps

进行注册https://cloud.google.com/打开网址进行注册

![](http://www.wangcong.online/upload/2019/3/image220190411024405263.jpeg)

我这边都注册了，现在没法出现那个注册页面了。但是基本上就是填写基本信息。信用卡号，有效期等等。然后当你提交这个页面后，一般银行会给你打电话问你是不是在谷歌云消费1美元，你回答是就行了。过一会这个1美元会返回你的账户。不必担心。

成功后出现如下页面点击查看控制台

![](http://www.wangcong.online/upload/2019/3/image320190411024405112.jpeg)

查看一下谷歌赠送我们的300刀是否到位

![](http://www.wangcong.online/upload/2019/3/image420190411024406290.png)

点击结算。

如图这个是我的结算用了好几天了，但是钱还是富富有余。你们的应该初始值是300刀

![](http://www.wangcong.online/upload/2019/3/image520190411024405300.jpeg)

下面开始是重点

开始创建VM实例

![](http://www.wangcong.online/upload/2019/3/image620190411024406389.png)

### 创建实例

![](http://www.wangcong.online/upload/2019/3/image720190411024406879.png)

后面就是具体创建实例的页面了。如图红框的部分是我们需要修改的。修改成如图的样子就好了。其他值都是默认就好，名称随便定义。

创建成功就会出现一个VM实例的列表，如图

![](http://www.wangcong.online/upload/2019/3/image820190411024406182.jpeg)

这里因为我之前创建过一个实例了，所以显示了2个。

### 验证速度（非必须步骤）

拷贝这个ip地址在浏览器输入[https://www.ipip.net/traceroute.php](https://www.ipip.net/traceroute.php)

![](http://www.wangcong.online/upload/2019/3/image920190411024406393.jpeg)

如图验证结果如下

![](http://www.wangcong.online/upload/2019/3/image1020190411024406753.jpeg)

速度均在100内，说明速度没问题。

### 配置服务器

连接ssh服务器，输入的命令如下：

1：手动输入  ：sudo –i （尽量手打）

2：请自行复制到记事本整理为一行在粘贴执行，切记哦

```
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocksR.sh&& chmod +x shadowsocksR.sh
```

3：然后执行一下命令

```
./shadowsocksR.sh
```

如图出现下图说明工作基本完成

![](http://www.wangcong.online/upload/2019/3/image1120190411024406634.png)

4：设置密码和端口

![](http://www.wangcong.online/upload/2019/3/image1220190411024406219.png)

5：一路回车后，大概需要几分钟左右的配置时间，等待就好。

![](http://www.wangcong.online/upload/2019/3/image1320190411024406828.png)

6：配置防火墙规则

网络-----VPC网络----防火墙规则

![](http://www.wangcong.online/upload/2019/3/image1420190411024406607.png)
把端口号设置为之前我们自己规定的789

![](http://www.wangcong.online/upload/2019/3/image1520190411024406585.jpeg)

如图，这里我之前设置了456，点进去都可以修改的。你之前设置的是多少就写多少

注意default-allow-http和default-allow-https 都需要点进去分别设置的 不要漏掉。

点进去修改这里，输入tcp:789; udp:789，点击保存

![](http://www.wangcong.online/upload/2019/3/image1620190411024407544.png)

四、如何使用：

百度“Shadowrocket”

https://github.com/shadowsocks/shadowsocks-windows

[https://github.com/shadowsocksrr/shadowsocksr-csharp/releases ](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)

