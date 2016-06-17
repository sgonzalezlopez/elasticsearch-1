from centos
MAINTAINER AXAMedLA

ENV http_proxy http://${proxyHost}:${proxyPort}
ENV https_proxy http://${proxyHost}:${proxyHost}

USER 0

RUN yum -y install java-1.7.0-openjdk

RUN wget --no-check-certificate https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.2.tar.gz
RUN tar -xf elasticsearch-0.90.2.tar.gz
RUN rm elasticsearch-0.90.2.tar.gz
 
EXPOSE :9300
EXPOSE :9200
 
CMD elasticsearch-0.90.2/bin/elasticsearch -f
