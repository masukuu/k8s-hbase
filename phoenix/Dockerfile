FROM openjdk:8-jdk

ENV HBASE_VERSION=2.5
ENV PHOENIX_VERSION=5.2.0
ENV PHOENIX_HOME=/opt/phoenix
ENV HBASE_HOME=/opt/hbase
ENV PATH=$PATH:$PHOENIX_HOME/bin

RUN wget -qO- https://dlcdn.apache.org/phoenix/phoenix-${PHOENIX_VERSION}/phoenix-hbase-${HBASE_VERSION}-${PHOENIX_VERSION}-bin.tar.gz | tar xvz -C /opt \
    && mv /opt/phoenix-hbase-${HBASE_VERSION}-${PHOENIX_VERSION}-bin $PHOENIX_HOME

COPY phoenix-queryserver-site.xml $PHOENIX_HOME/bin/

EXPOSE 8765

CMD ["queryserver.py"]
#  https://dlcdn.apache.org/phoenix-5.2.0/phoenix-hbase-2.5-5.2.0-bin.tar.gz 

#  https://dlcdn.apache.org/phoenix/phoenix-5.2.0/phoenix-hbase-2.5-5.2.0-bin.tar.gz
