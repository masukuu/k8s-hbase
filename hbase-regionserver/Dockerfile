# 使用基礎映像
FROM openjdk:8-jdk

# 設置環境變量
ENV HBASE_VERSION=2.5.8
ENV HBASE_HOME=/opt/hbase

# 下載並解壓 HBase
RUN wget -qO- http://archive.apache.org/dist/hbase/${HBASE_VERSION}/hbase-${HBASE_VERSION}-bin.tar.gz | tar xvz -C /opt \
    && mv /opt/hbase-${HBASE_VERSION} ${HBASE_HOME} \
    && rm -rf ${HBASE_HOME}/docs \
    && rm -rf ${HBASE_HOME}/src

# 將 HBase 添加到 PATH 中
ENV PATH=$PATH:${HBASE_HOME}/bin

# 複製 HBase 配置文件
COPY hbase-site.xml ${HBASE_HOME}/conf/

# 暴露端口
EXPOSE 16020 16030

# 啟動 HBase RegionServer
CMD ["hbase", "regionserver", "start"]
