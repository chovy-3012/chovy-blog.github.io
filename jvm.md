# JVM

## 常用参数

```shell
## 设置内存大小
-Xms16g -Xmx32g -server 
## 使用G1垃圾回收期
-XX:+UseG1GC -XX:MaxGCPauseMillis=50  
## 打印GC日志
-verbose:gc -XX:+PrintGCDetails -XX:+PrintGCDateStamps -Xloggc:$KYLIN_HOME/logs/kylin.gc.log-`date +'%Y%m%d%H%M'` -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=12 -XX:GCLogFileSize=128M 
## 开启JMX端口
-Dcom.sun.management.jmxremote.ssl=false -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.port=7778
## 开启远程调试
-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=11000
## full gc前打印堆文件
-XX:+HeapDumpBeforeFullGC -XX:HeapDumpPath=/var/log/hbase/dump.hprof
```

