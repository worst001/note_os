# Linux与Mac常见问题

## [制作与使用源](https://blog.csdn.net/Homewm/article/details/80642851)

## 常用命令

`netstat -tnlp`                       : 查看端口占用

`ss -tnlp`                            : 查看端口占用

`du -sh * | sort -rh`                 : 查看硬盘空间

`lscpu`                               : 查看CPU基本信息

`cat /proc/cpuinfo`                   : 查看CPU详细信息

`free -m`                             : 查看内存基本信息

`cat /proc/meminfo`                   : 查看内存详细信息

`lsblk`                               : 查看硬盘基本信息

`lsb_release -a`                      : 查看操作系统信息

`cat /etc/redhat-release`             : 查看红帽系列操作系统版本

`service sshd restart`                : 重启 ssh 服务

`vi /etc/resolv.conf`                 : DNS 的配置文件

`:w !sudo tee %`                      : 保存只读文件

`sudo usermod -a -G microk8s ubuntu`  : 将ubuntu 用户加到microk8s组

`caffeinate -disu -w 0`               : 关闭自动休眠

`sudo pmset -a disablesleep 1`        : 关闭休眠状态

`lsof -nP -p 1293`                    : 根据进程号查看端口


## ssh
1. 配置信任列表( 公钥 )
`/root/.ssh/authorized_keys`

2. FTP 配置的坑
需要注释掉pam机制
`#auth    required pam_shells.so`

3. GSSAPIAuthentication认证的坑
+ SSH 默认开启了 GSSAPIAuthentication 认证
+ 一般 SSH 依次进行的认证方法的是 publickey, gssapi-keyex, gssapi-with-mic, password， 这个你可以ssh -v开启 debug 模式在连接日志看到。
+ 一般用户只使用 password 认证方式，但前面 3 个认证过程系统还是会尝试，这就浪费时间了，也就造成 SSH 登录慢。
+ 关于 GSSAPI 相关的认证，消耗的时间比较多，具体可以查看 SSH 连接日志。
+ GSSAPI 主要是基于 Kerberos 的，因此要解决这个问题也就变成要系统配置有 Kerberos， 一般用户是没有配置 Kerberos的，所以那就直接把 SSH 服务端的 GSSAPIAuthentication 直接关掉吧，客户端也可以关掉。

## 设置时区与时间同步
1. `tzselect` 选择时区
2. `sudo timedatectl set-timezone 'Asia/Shanghai'` 设置时区
3. `ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime` 设置本地时间
4. `watch -n 1 date` 实时刷新并查看当前时间
5. `ntpdate -dv 210.72.145.44` 向国家授时中心服务器申请时间同步


## Linux Kernel 的坑
1. 配置的坑
    + 本地和服务器的时区需要一致
    + 可能被已被封锁
    + modprobe黑名单导致
    + 黑名单中的模块再加载不到
        > Linux内核版本中没有默认的模块
        > 加入其它版本内核的 `.ko` 模块后运行 `depmod`
        > 模块路径需要一致
2. 升级内核
3. 通过 `secure`(log) `openswan.log` `pluto.log `分析接入日志和ipsec上的解析加密日志


## [SELinux的三种模式](https://blog.csdn.net/haohaoxuexiyai/article/details/113886865)

## Crontab 任务
`crontab -e` 编辑任务 使用用绝对路径保证脚本正确执行
| *    | *    | *    | *    | *    | command |
|------|------|------|------|------|---------|
| 分　 | 时　 | 日　 | 月　 | 周   | 命令    |

## 分卷压缩
> SIZE: 可以是 10m 5k 等

zip -s SIZE origin.zip --out new.zip

zip - largefile | split -b SIZE

zip - largefile | split -b SIZE -a 3 - file.zip

## Tmux 的坑
旧版Centos缺失 libevent 库库时
[libevent配置](https://blog.csdn.net/yesuhuangsi/article/details/100543261)


