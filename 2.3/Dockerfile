from centos
MAINTAINER AXAMedLA

USER 0

#RUN yum -y install java-1.7.0-openjdk

#ADD jdk-7u79-linux-x64.rpm .
RUN cd /tmp \
&& curl --digest -x ${http_proxy} --user ${REPO_USER}:${REPO_PASS} -LO http://filerepo.osappext.pink.eu-central-1.aws.openpaas.axa-cloud.com/liferay-docker/jdk-7u79-linux-x64.rpm \
&& rpm -i /tmp/jdk-7u79-linux-x64.rpm \
&& rm -f /tmp/jdk-7u79-linux-x64.rpm

RUN wget --no-check-certificate https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.2.tar.gz
RUN tar -xf elasticsearch-0.90.2.tar.gz
RUN rm elasticsearch-0.90.2.tar.gz
 
EXPOSE :9300
EXPOSE :9200
 
CMD elasticsearch-0.90.2/bin/elasticsearch -f
