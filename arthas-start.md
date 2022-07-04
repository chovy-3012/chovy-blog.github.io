# Arthas

## 下载

```shell
curl -O https://arthas.aliyun.com/arthas-boot.jar
java -jar arthas-boot.jar
```

命令 https://arthas.gitee.io/advanced-use.html

## 监控相关

### monitor

监控方法执行时间和成功失败

### watch

监控方法入参/返回值/耗时等信息

```shell
watch org.apache.hadoop.hive.metastore.HiveMetaStore$HMSHandler firePreEvent "{params,returnObj}" -x 3
```



### trace

方法内部调用路径，并输出方法路径上的每个节点上耗时

```shell
trace org.apache.hadoop.hive.metastore.HiveMetaStore$HMSHandler get_database

##耗时
trace org.apache.hadoop.hive.metastore.HiveMetaStore$HMSHandler get_database -n  1000 '#cost > 1000'
```



### tt

