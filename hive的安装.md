## hive的安装

1. 下载地址

   http://www.apache.org/dyn/closer.cgi/hive/

2. 文档

   https://cwiki.apache.org/confluence/display/Hive/GettingStarted

### 安装部署

1. 准备

   ```
   apache-hive-3.1.2-bin.tar.gz
   mysql-5.6.47-linux-glibc2.12-x86_64.tar.gz
   mysql-connector-java-5.1.45.jar
   ```

   

2. 解压hive安装包

   ```
    tar -zxvf apache-hive-3.1.2-bin.tar.gz
   ```

3. 配置环境变量

   ```
   vim /etc/profile
   
   export HIVE_HOME=/opt/bigdata/apache-hive-3.1.2-bin
   export PATH=$PATH:$HADOOP_HOME/bin:$HADOOP_HOME/sbin:$JAVA_HOME/bin:$HIVE_HOME/bin
   
   配置生效：source /etc/profile
   ```

4. 解决日志jar冲突

   ```
   [root@node01 apache-hive-3.1.2-bin]# mv $HIVE_HOME/lib/log4j-slf4j-impl-2.10.0.jar  $HIVE_HOME/lib/log4j-slf4j-impl-2.10.0.jar_bak
   
   ```

   

5. 初始化元数据库

   ```
   bin/schematool  -dbType derby -initSchema
   ```

6. 启动并使用hive

   ```
   先启动hdfs
   start-dfs.sh
   
   然后启动yarn
   
   ```

   









