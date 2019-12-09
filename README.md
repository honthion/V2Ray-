# V2Ray-



## ssl配置

https://www.hi-linux.com/posts/6968.html

```shell
# 下载 Certbot 客户端
$ wget https://dl.eff.org/certbot-auto

# 设为可执行权限
$ chmod a+x certbot-auto

# 申请通配符证书
./certbot-auto certonly  -d "*.papiloop.co" --manual --preferred-challenges dns-01  --server https://acme-v02.api.letsencrypt.org/directory

#certonly 表示插件，Certbot 有很多插件。不同的插件都可以申请证书，用户可以根据需要自行选择。
#-d 为哪些主机申请证书。如果是通配符，输入 *.xxx.com (根据实际情况替换为你自己的域名)。
#--preferred-challenges dns-01，使用 DNS 方式校验域名所有权。
#--server，Let's Encrypt ACME v2 版本使用的服务器不同于 v1 版本，需要显示指定。



dig  -t txt _acme-challenge.bwg0701.papiloop.co @8.8.8.8 
yum install bind-utils

```



## 配置

https://tlanyan.me/v2ray-traffic-mask/
