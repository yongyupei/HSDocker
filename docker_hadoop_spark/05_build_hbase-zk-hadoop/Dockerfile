FROM 202.116.46.215/hsdocker2019/hs_zk-hadoop:v1.0
COPY hbase_config/* /tmp/
RUN wget http://50125.hnbdata.cn:81/common/hsdocker/hbase-1.2.6-bin.tar.gz -O /tmp/hbase-1.2.6-bin.tar.gz && \
	tar -zxvf /tmp/hbase-1.2.6-bin.tar.gz && \
    mv hbase-1.2.6 /usr/local/hbase && \
    rm /tmp/hbase-1.2.6-bin.tar.gz
ENV HBASE_HOME=/usr/local/hbase
ENV PATH=$PATH:$HBASE_HOME/bin
ENV JAVA_TOOL_OPTIONS=-Dfile.encoding=UTF8
RUN mv /tmp/hbase-env.sh $HBASE_HOME/conf && \
    mv /tmp/hbase-site.xml $HBASE_HOME/conf && \
    mv /tmp/regionservers $HBASE_HOME/conf && \
    . /etc/profile
CMD exec /bin/bash -c "service ssh start;trap : TERM INT; sleep infinity & wait"