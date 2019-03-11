## 官网下载相关文件

<http://product.mftcc.cn/rdp/download.html>[](http://product.mftcc.cn/rdp/download.html)

下载“免配置64位”和“v2.3.\*数据库”

![](http://www.wangcong.online/upload/2018/11/ss9apo048sgpqqb0q8n05gkb73.png)

## 启动报表数据库：

解压数据库压缩文件：MYSQL_RDP.zip

执行MYSQL_RDP\\mysql_rdp-server\\初始化并启动数据库.bat（==注意不能关闭该窗口==）

启动成功如下图：

![](http://www.wangcong.online/upload/2018/11/op7e0mto4giinq8bbijnj75lsk.png)

数据库名称：rdp_server

用户名：root

密 码：root

端口号：3378

## 启动项目

解压BDDPx64.zip 执行BDDPx64\\启动.bat。

也可直接去内置tomcat启动startup.bat。

启动成功如下图：

![](http://www.wangcong.online/upload/2018/11/5mbgqku2fsifqq38as1bd0n24i.png)

## 配置基础数据（这步可以先不看）

修改\*.yml文件一定要先了解，yml文件的格式，不要乱改，只改下面说的地方就可以了

注：默认配置是使用相对路径的，路径直接映射到“BDDPx64\\data\\”这个文件夹下数据文件，如果不需要给报表配置文件单独分配保存目录，建议不要修改相关配置

以下配置是不使用相对路径的配置方式

1.找到 BDDPx64\\webapps\\RDP-SERVER\\WEB-INF\\classes\\application.yml 文件

2.将“relative-path”这个属性值修改为 false

3.修改 application.yml 文件中的

bddp:data-path、bddp:map-path、rdp:data-path的路径分别指向BDDPx64下的data文件夹的对应目录，如图：

注：路径结尾一定要有“/”，2.3.3之后不加也可以了

![](http://www.wangcong.online/upload/2018/11/vv2e5grfo2il7remnjdtenvj0j.png)

注意：2.3.3之后版本大屏幕报表的路径配置合并为一个了

如下填写就行

![](http://www.wangcong.online/upload/2018/11/1btph1fj9oi0krvdol6eqkalab.png)

## 访问项目

浏览器地址输入：<http://localhost:8080/RDP-SERVER/>[](http://localhost:8080/RDP-SERVER/)

![](http://www.wangcong.online/upload/2018/11/5knnpg8d6agrdopg464jf8p6c0.png)

用户名：admin 密码：admin 必须输入验证码

管理员：admin/admin

开发人员：user/000000

业务人员: guest/000000

## 授权报表系统

1.使用admin账户，登录报表系统

2.点击系统管理->授权信息，打开授权查看页面

![](http://www.wangcong.online/upload/2018/11/5occ7uqammj5loruf9brt9i1lp.png)  

3.点击激活按钮，复制机器码，按照提示操作，获取授权码

![](http://www.wangcong.online/upload/2018/11/4miah8906cjv9o30a0mkhpkvdj.png)  

4.激活系统

![](http://www.wangcong.online/upload/2018/11/u3kpcftchsibupbt8579sdiu5i.png)  

5刷新页面查看激活情况

![](http://www.wangcong.online/upload/2018/11/u2p5027jaeif3rneg91nl30f8k.png)  


