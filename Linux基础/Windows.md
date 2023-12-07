# Windows 命令

## 进程

1. 查看某个进程的详细信息

```ps
wmic process where caption="java.exe" get processid,caption,commandline /value
```

2. 查看进程列表
```ps
tasklist|findstr "java"
```

3. 杀死进程
```ps
taskkill /F /pid $PID -t
```
/F: 强制关闭

4. 查看进程对应端口
```ps
netstat -ano|findstr "8080"
```

5. 通过 gpedit.msc [配置策略](https://new.qq.com/omn/20220107/20220107A02GQ400.html)
