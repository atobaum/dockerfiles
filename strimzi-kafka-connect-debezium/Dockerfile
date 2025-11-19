# ref. https://strimzi.io/blog/2020/01/27/deploying-debezium-with-kafkaconnector-resource/
FROM quay.io/strimzi/kafka:0.48.0-kafka-4.1.0

USER root:root

RUN mkdir -p /opt/kafka/plugins/debezium

ADD https://repo1.maven.org/maven2/io/debezium/debezium-connector-mysql/3.2.1.Final/debezium-connector-mysql-3.2.1.Final-plugin.tar.gz /opt/kafka/plugins/debezium/
ADD https://repo1.maven.org/maven2/io/debezium/debezium-connector-mongodb/3.2.1.Final/debezium-connector-mongodb-3.2.1.Final-plugin.tar.gz /opt/kafka/plugins/debezium/
RUN tar -xvf /opt/kafka/plugins/debezium/debezium-connector-mysql-3.2.1.Final-plugin.tar.gz -C /opt/kafka/plugins/debezium/
RUN tar -xvf /opt/kafka/plugins/debezium/debezium-connector-mongodb-3.2.1.Final-plugin.tar.gz -C /opt/kafka/plugins/debezium/

USER 1001
