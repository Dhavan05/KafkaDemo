# KafkaDemo
Basic Kafka program to send and receive messages

Step 1: Download the code
> tar -xzf kafka_2.12-2.5.0.tgz
> cd kafka_2.12-2.5.0

Step 2: Start the server
> bin/zookeeper-server-start.sh config/zookeeper.properties

Step 3: Create a topic
> bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test
