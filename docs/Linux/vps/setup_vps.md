---
title: vps 搭建ssr + bbr
lang: zh
---

# 环境 Ubuntu 18.10 x64

# 安装
```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```
- 选择安装 shadowsocks-python
- 设置 密码
- 设置 端口
- 设置 加密方式 aes-256-cfb
# shadowsocks命令
```
/etc/init.d/shadowsocks start | stop | restart | status
```
# shadowsocks配置文件路径
```
/etc/shadowsocks-python/config.json
```

# 开启bbr加速
```
wget –no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
```
# 查看bbr状态
```
lsmod | grep bbr
```
>返回值 tcp_bbr 即开启成功