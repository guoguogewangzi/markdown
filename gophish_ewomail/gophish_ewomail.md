ewomail安装：

![image-20220424011504988](assets/image-20220424011504988.png)



![image-20220424011526730](assets/image-20220424011526730.png)





ewomail访问地址：

![image-20220424011418771](assets/image-20220424011418771.png)



/etc/hosts设置

![image-20220424004522272](assets/image-20220424004522272.png)



域名解析设置

![image-20220424012802951](assets/image-20220424012802951.png)



`telnet smtp.qq.com 25`测试

![image-20220424004608929](assets/image-20220424004608929.png)







修改gophish配置文件：`config.json`,将127.0.0.1改为：0.0.0.0:3333，0.0.0.0:80改为0.0.0.0:81为了与ewomail的web客户单80端口错开

![image-20220424011036727](assets/image-20220424011036727.png)



gophish登录

![image-20220424005710494](assets/image-20220424005710494.png)

启动时，存在用户名:`admin`,密码:`3529d8a5288cfc1c`

![image-20220424005754087](assets/image-20220424005754087.png)









gophish设置

![image-20220424005133463](assets/image-20220424005133463.png)

解释：

Name:随便填

From:发邮件人



该发件人存在ewomail邮件服务器中的邮件r人：test@guoguogewangzi.com

![image-20220424005254183](assets/image-20220424005254183.png)



Host:发邮件的邮件服务器

Password:刚刚填写的发件人的邮件登录密码



收件人：`879086359@qq.com`,发送成功

![image-20220424010042072](assets/image-20220424010042072.png)



数据包：邮件服务器`10.2.12.6（内网ip）`向`218.19.148.195:25（smtp.*.com:25）`发包

![image-20220424004731528](assets/image-20220424004731528.png)



总结，gophish利用自搭平台ewomail邮件服务器，创建的邮件账号：test@guoguogewangzi.com，向收件人:879086359@qq.com,发送邮件，邮件内容可含恶意链接，故称钓鱼



利用smtp.qq.com:25服务器发送钓鱼邮件

![image-20220424011614318](assets/image-20220424011614318.png)



password：需发送短获取，发送之后点击我已发送，显示码出来后，然后再点击确定

![image-20220424011921147](assets/image-20220424011921147.png)



发送成功，可以自己发给自己

![image-20220424011745561](assets/image-20220424011745561.png)





参考：

https://www.freebuf.com/articles/web/260391.html

https://github.com/gyxuehu/EwoMail

安装ewomail

http://doc.ewomail.com/docs/ewomail/install

内部通信

http://doc.ewomail.com/docs/ewomail/local_con