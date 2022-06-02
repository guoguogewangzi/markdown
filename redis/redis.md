安装

参考：
https://www.runoob.com/redis/redis-install.html



Windows版下载地址：
https://github.com/tporadowski/redis/releases



如：
Redis-x64-5.0.14.1.zip

![image-20220602150058284](redis.assets/image-20220602150058284.png)



解压即可用：

![image-20220602150135866](redis.assets/image-20220602150135866.png)





启动服务器：
redis-server.exe redis.windows.conf

![image-20220602150235472](redis.assets/image-20220602150235472.png)





客户端连接
redis-cli.exe -h 127.0.0.1 -p 6379

![image-20220602150321968](redis.assets/image-20220602150321968.png)



连接成功：

![image-20220602150339015](redis.assets/image-20220602150339015.png)





连接不成功，如：

![image-20220602150421177](redis.assets/image-20220602150421177.png)

身份认证，auth+密码

![image-20220602150507302](redis.assets/image-20220602150507302.png)





