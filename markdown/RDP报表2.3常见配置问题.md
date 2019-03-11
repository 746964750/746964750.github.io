## RDP报表部署环境

Tomcat7+、JDK8、MySQL5.5+

## RDP报表授权去除水印

![](http://www.wangcong.online/upload/2018/11/1u6n5bhg0chqbqbkl62h1kor88.png)![](http://www.wangcong.online/upload/2018/11/t4nvru3of0hnmqhpgsuqb9klhq.png)

## linux系统部署验证码显示不正常

![](http://www.wangcong.online/upload/2018/11/5uqpsa428ug1dpsntct0gkn8dq.png)

百度“修改linux默认字体”

## 自带的DEMO打不开

1.首先确认项目正常启动

2.登录系统点击“公共数据源配置”，找到“report_demo”这个数据源

3.修改report_demo内容，注意连接地址是否正确，尤其是端口号，report_demo数据库包含在“MYSQL_RDP”中

4.如数据库未做修改，如下填写即可

![](http://www.wangcong.online/upload/2018/11/1tlqh80k0ehmnp68tq6a57cr8s.png)

## 模板解析失败、保存成功但是查找不到，可能的情况

1.模版路径配置有问题，模板路径最后一定要“/”结尾，如图

![](http://www.wangcong.online/upload/2018/11/tor8ht207ojtnpcsqcecq6n2fq.png)

## 报表系统更新，需要备份的文件

1.data路径所有文件备份

2.将备份文件复制替换到新项目中即可