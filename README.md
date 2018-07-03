# kafka_producer_consumer

How to create executable kafka producer and comsumer
1) Checkout the code from https://github.com/bala-aark/kafka_producer_consumer.git
2) Go to the folder kafka_producer_consumer
3) ./gradlew clean
4) ./gradlew producer
5) ./gradlew consumer

Make sure the following jar files are generated in build/libs folder
1) kafka-consumer-0.1.jar
2) kafka-producer-0.1.jar

Steps to verify kafka producer and consumer
1) Start zookeeper from kafka installation folder
	bin/zookeeper-server-start.sh config/zookeeper.properties
2) Start kafka server from kafka installation folder
	bin/kafka-server-start.sh config/server.properties
3) Create topic
	bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1  --partitions 1 --topic <<topic name>>
4) Start producer from application folder
	java -jar build/libs/kafka-consumer-0.1.jar <<topic name>>
5) Start consumer from application folder
	java -jar build/libs/kafka-producer-0.1.jar <<topic>>
