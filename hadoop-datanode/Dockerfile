FROM openjdk:8-jdk

ENV HADOOP_VERSION=3.4.0
ENV HADOOP_HOME=/opt/hadoop
ENV PATH=$PATH:$HADOOP_HOME/bin

RUN wget -qO- https://downloads.apache.org/hadoop/common/hadoop-$HADOOP_VERSION/hadoop-$HADOOP_VERSION-src.tar.gz | tar xvz -C /opt \
    && mv /opt/hadoop-$HADOOP_VERSION-src $HADOOP_HOME

COPY core-site.xml $HADOOP_HOME/etc/hadoop/
COPY hdfs-site.xml $HADOOP_HOME/etc/hadoop/

EXPOSE 9864

CMD ["hdfs", "datanode"]
