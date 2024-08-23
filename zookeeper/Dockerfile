FROM openjdk:8-jdk

ENV ZOOKEEPER_VERSION=3.8.4
ENV ZOOKEEPER_HOME=/opt/zookeeper
ENV PATH=$PATH:$ZOOKEEPER_HOME/bin

RUN wget -qO- https://downloads.apache.org/zookeeper/zookeeper-$ZOOKEEPER_VERSION/apache-zookeeper-$ZOOKEEPER_VERSION-bin.tar.gz | tar xvz -C /opt \
    && mv /opt/apache-zookeeper-$ZOOKEEPER_VERSION-bin $ZOOKEEPER_HOME

COPY zoo.cfg $ZOOKEEPER_HOME/conf/

EXPOSE 2181 2888 3888

CMD ["zkServer.sh", "start-foreground"]
