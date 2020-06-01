# KafkaDemo
Basic Kafka program to send and receive messages : Windows

Step 1: Download the code
> tar -xzf kafka_2.12-2.5.0.tgz
> cd kafka_2.12-2.5.0

Step 2: Start the server
> bin\windows\zookeeper-server-start.bat config\zookeeper.properties
> bin\windows\kafka-server-start.bat config\server.properties

Step 3: Create a topic
> bin\windows\kafka-topics.bat --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic test
  To List Topics
  > bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092

Step 4: Producer - Send message
> bin\windows\kafka-console-producer.bat --bootstrap-server localhost:9092 --topic test

Step 5: Consumer - Receive messages
> bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic test --from-beginning
