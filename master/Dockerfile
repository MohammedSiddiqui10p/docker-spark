FROM bde2020/spark-base:2.4.3-hadoop2.7

MAINTAINER Erika Pauwels <erika.pauwels@tenforce.com>
MAINTAINER Gezim Sejdiu <g.sejdiu@gmail.com>

COPY master.sh /

ENV SPARK_MASTER_PORT 7077
ENV SPARK_MASTER_WEBUI_PORT 8080
ENV SPARK_MASTER_LOG /spark/logs

# apache livy
RUN wget http://us.mirrors.quenda.co/apache/incubator/livy/0.6.0-incubating/apache-livy-0.6.0-incubating-bin.zip -O /tmp/livy.zip
RUN mkdir -p /opt
RUN unzip /tmp/livy.zip -d /opt/
# Logging dir
RUN mkdir /opt/apache-livy-0.6.0-incubating-bin/logs

EXPOSE 8080 7077 6066 8998

CMD ["/bin/bash", "/master.sh"]
