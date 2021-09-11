---
title: "iOS 中安装 SSH 及常用终端工具"
date: 2012-11-14T14:56:31+08:00
# bookComments: false
# bookSearchExclude: false
---

1. 使用 Cydia 搜索并安装 OpenSSH。

2. 使用 Cydia 搜索并安装 MobileTerminal Package。

3. 使用 Cydia 安装 apt 0.7 strict, apt 0.7 strict(lib), apt 0.7 HTTPS Method, apt 0.7(apt-key)。

4. 使用 MobileTerminal 登录。
    - root 默认密码：`alpine`
    - mobile 默认密码：`alpine`

## 启动 MobileTerminal 安装常用工具
```bash
su root    # 然后输入root密码
> apt-get install inetutils      # ping 命令需要
> apt-get install ifconfig
> apt-get install netstat
> apt-get install more
> apt-get install vim
```
