FROM openjdk:8-jdk

ENV HIVE_VERSION=3.1.2
ENV HIVE_HOME=/opt/hive
ENV HADOOP_HOME=/opt/hadoop
ENV PATH=$PATH:$HIVE_HOME/bin:$HADOOP_HOME/bin

RUN wget -qO- https://downloads.apache.org/hive/hive-$HIVE_VERSION/apache-hive-$HIVE_VERSION-bin.tar.gz | tar xvz -C /opt \
    && mv /opt/apache-hive-$HIVE_VERSION-bin $HIVE_HOME

COPY hive-site.xml $HIVE_HOME/conf/

EXPOSE 10000

CMD ["hive", "metastore"]
