# Kafka Quick Start Guide

This guide will walk you through the steps to download, install, and set up Kafka on a Windows system. Kafka is a distributed streaming platform that allows you to publish and subscribe to streams of records in real-time.

## Step 1: Download and Install Kafka

1. Go to the Kafka website to download the latest version:
   [Kafka Downloads](https://kafka.apache.org/downloads)

2. Once the download is complete, extract the contents of the downloaded file to your desired installation location.

## Step 2: Start the Kafka Environment

1. Open a command prompt or terminal window.

2. Navigate to the Kafka installation directory.

3. Start the ZooKeeper service by running the following command:

``.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties``

4. Start the Kafka broker service by running the following command:

``.\bin\windows\kafka-server-start.bat .\config\server.properties``

## Step 3: Create a Topic to Store Your Events

To use Kafka, you need to create a topic where your events will be stored.

1. Open a new command prompt or terminal window.

2. Navigate to the Kafka installation directory if you are not already there.

3. Run the following command to create a topic named "topic_demo" on your Kafka broker:

``.\bin\windows\kafka-topics.bat --create --topic topic_demo --bootstrap-server localhost:9092``


## Step 4: Write Some Events Into the Topic

Now that you have a topic, you can start writing events into it.

1. Open a new command prompt or terminal window.

2. Navigate to the Kafka installation directory if you are not already there.

3. Run the following command to start the Kafka console producer and begin writing events to the "topic_demo" topic:

``.\bin\windows\kafka-console-producer.bat --topic topic_demo --bootstrap-server localhost:9092``

## Step 5: Read the Events

To read the events from the topic, you need to start the Kafka console consumer.

1. Open a new command prompt or terminal window.

2. Navigate to the Kafka installation directory if you are not already there.

3. Run the following command to start the Kafka console consumer and read the events from the beginning of the "topic_demo" topic:

``.\bin\windows\kafka-console-consumer.bat --topic topic_demo --from-beginning --bootstrap-server localhost:9092``


Now, you should be able to see the events that you wrote in Step 4 being consumed by the console consumer.

For more advanced usage and integration with Spring Boot applications, you can refer to the [Spring Kafka documentation](https://docs.spring.io/spring-kafka/reference/html/#spring-boot-consumer-app).

Congratulations! You have successfully set up Kafka and performed basic operations with it. Happy streaming!
