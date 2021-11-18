以管理员身份执行cmd，执行下列命令。

```
// 将127.0.0.1 80的请求转发至10.0.40.100 80
netsh  interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=80 connectaddress=10.0.40.100 connectport=80

// 查看所有的侦听端口
netsh interface portproxy show all

// 删除某条规则
netsh interface portproxy delete v4tov4 listenaddress=127.0.0.1 listenport=80
```



__使用netsh interface portproxy记得配置Windows和出口路由器防火墙规则__