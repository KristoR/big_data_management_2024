FROM pyspark-delta:0.0.1

USER root

RUN wget -P /usr/local/spark/jars/ https://repo1.maven.org/maven2/org/apache/spark/spark-sql-kafka-0-10_2.12/3.5.0/spark-sql-kafka-0-10_2.12-3.5.0.jar && \
    chmod 644 /usr/local/spark/jars/spark-sql-kafka-0-10_2.12-3.5.0.jar && \
    wget -P /usr/local/spark/jars/ https://repo1.maven.org/maven2/org/apache/kafka/kafka-clients/3.4.0/kafka-clients-3.4.0.jar && \
    chmod 644 /usr/local/spark/jars/kafka-clients-3.4.0.jar && \
    wget -P /usr/local/spark/jars/ https://repo1.maven.org/maven2/org/apache/spark/spark-streaming-kafka-0-10-assembly_2.12/3.5.0/spark-streaming-kafka-0-10-assembly_2.12-3.5.0.jar && \
    chmod 644 /usr/local/spark/jars/spark-streaming-kafka-0-10-assembly_2.12-3.5.0.jar && \
    wget -P /usr/local/spark/jars/ https://repo1.maven.org/maven2/org/apache/commons/commons-pool2/2.12.0/commons-pool2-2.12.0.jar && \
    chmod 644 /usr/local/spark/jars/commons-pool2-2.12.0.jar && \
    rm /usr/local/spark/jars/commons-pool-1.5.4.jar && \
    pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir python-dotenv>=1.0.1

USER ${NB_UID}