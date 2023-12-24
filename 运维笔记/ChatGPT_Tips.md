## Hive节点磁盘满时的处理步骤

当Hive节点的磁盘满时，您可以采取以下几个步骤来清理长时间未使用的冗余数据：

### 查找大文件或目录

使用`du`和`find`命令来找出占用磁盘空间较大的文件或目录。

```bash
# 查找大于特定大小（比如1G）的文件
find / -type f -size +1G -exec ls -lh {} \;

# 查找HDFS中大文件
hadoop fs -du -h /user/hive/warehouse | sort -h

# 分析磁盘使用情况，找出使用空间最多的目录
du -h --max-depth=1 / | sort -hr
```

### 清除操作日志和临时文件

删除Hive节点上的操作日志文件和临时文件，这通常不会影响数据在HDFS中的状态。

```bash
# 清除Hive日志
rm -rf /var/log/hive/*

# 清除临时文件
rm -rf /tmp/*
```

### 删除无用的表和分区

在Hive元数据中标记为删除状态的表和分区实际上在HDFS上可能仍然存在。

使用Hive命令行，运行以下命令来删除老旧的表和分区：

```sql
# 登录Hive命令行
hive

# 列出并评估需要删除的冗余表格
SHOW TABLES;

# 删除无用的表
DROP TABLE IF EXISTS [table_name];

# 删除无用的分区
ALTER TABLE [table_name] DROP PARTITION ([partition_spec]);
```
**注**: 替换 `[table_name]` 和 `[partition_spec]` 为具体的表名和分区定义。

### 运行HDFS清理命令

如果Hive项的表和分区已经从元数据中删除，但相关的HDFS数据尚未清除，您需要进行手动清理。

```bash
# 手动删除HDFS中的数据
hadoop fs -rm -r /user/hive/warehouse/[database_name].db/[table_name]

# 清理垃圾回收站
hadoop fs -expunge
```

### 清理HDFS中的冗余数据

HDFS可能存储了许多冗余数据，如临时文件、已删除但尚未清除的数据块。

使用hdfs dfs命令清理这部分数据：

```bash
# 清理.tmp目录
hadoop fs -rm -r /tmp/*

# 清理垃圾回收站（Trash），在安全模式下才能执行
hadoop fs -expunge

# 清除HDFS中断开的文件
hdfs fsck / | grep 'Under replicated' | awk -F':' '{print $1}' | xargs -I {} hadoop fs -rm {}
```

### 确认数据是否可以删除

在删除任何文件或HDFS数据之前，确保它们不是重要或者仍在使用的。检查后备份或归档不常访问但仍需要保留的数据。

### 设置数据生命周期管理和清洁作业

这是一个预防措施。设置定期清洁任务来预防未来的磁盘空间问题。你可以利用Apache Oozie来安排定期的清洁作业。

完成上述步骤后，检查磁盘空间是否有足够的释放，如果没有，则可能需要检查其他应用程序或日志文件，或者可能需要考虑增加更多的磁盘空间或优化现有空间的使用。在企业环境中，务必与数据管理员或系统管理员协调，以确保与公司的数据保护策略和流程相一致。
