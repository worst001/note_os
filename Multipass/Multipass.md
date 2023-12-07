# Multipass
> Ubuntu 微虚拟机

## 基础命令

`multipass launch --name microk8s-vm --mem 4G --disk 40G` : 创建虚拟机内存 4G 最大磁盘 40G

`multipass shell microk8s-vm`                             : 进入虚拟机 microk8s-vm 的 shell

`multipass exec microk8s-vm -- sudo ll`                   : 从外部执行 microk8s-vm 内的 ll 命令
