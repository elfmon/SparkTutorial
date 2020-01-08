FROM openjdk:8-alpine
RUN apk --update add wget tar bash
RUN wget https://www-eu.apache.org/dist/spark/spark-2.4.4/spark-2.4.4-bin-hadoop2.7.tgz
RUN tar -xzf spark-2.4.4-bin-hadoop2.7.tgz && \
    mv spark-2.4.4-bin-hadoop2.7 /spark && \
    rm spark-2.4.4-bin-hadoop2.7.tgz
COPY start-master.sh /start-master.sh
COPY start-worker.sh /start-worker.sh
RUN chmod +x start-master.sh && chmod +x start-worker.sh
