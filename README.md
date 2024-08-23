# k8s-hbase

Iamge: https://hub.docker.com/repository/docker/linboso/hbase-master-2.5.8/general

## action item
- [ ] 建立 HBase 1 部 region server 可以 read/write 
- [ ] 建立 2 部 region server，皆可 read/ write  
- [ ] 建立 4 部 region server，皆可 read/ write  
- [ ] 確認 Phoenix 功能 
- [ ] 確定 HDFS 映射實體主機磁碟位置
- [ ] 確認 Hive 功能 
- [ ] 建立 HBase Backup  

## test 
1. 使用 Docker compose 建立 pseudo distribution HBase 其中包含。 
    1. masterserver x 1 
    2. regionserver x 2
    3. zookeeper    x 1
    4. namenode     x 1
    5. datanode     x 1
2. 使用 k8s 建立 fully distribution HBase 其中包含
    1. masterserver x 2
    2. regionserver x 3
    3. zookeeper    x 1
    4. namenode     x 1
    5. datanode     x 1

## deploy 
使用 k8s 建立 fully distribution HBase 其中包含
1. masterserver x 2 
2. regionserver x 3
3. zookeeper    x 1
4. namenode     x 1 ?
5. datanode     x 1 ?
6. phoenix      x 1
7. hive         x 1
    

## Docker Image
- [ ] master server
    - [ ] config file
- [ ] region server
    - [ ] config file
- [ ] zookeeper
- [ ] HDFS
    - [ ] namenode
        - [ ] config file
    - [ ] datanode
        - [ ] config file

- [ ] SQL engine 
    - [ ] phoenix
    - [ ] hive


## Ref
1. [hbase-site.xml 1](https://github.com/apache/hbase/blob/master/hbase-common/src/main/resources/hbase-default.xml)
2. [hbase-site.xml 2](https://blog.csdn.net/appleyuchi/article/details/106141175)
3. [hdfs-site.xml 1](https://github.com/hanborq/hadoop/blob/master/example-confs/conf.secure/hdfs-site.xml)
4. [hdfs-site.xml 2](https://hadoop.apache.org/docs/r2.4.1/hadoop-project-dist/hadoop-hdfs/hdfs-default.xml)


