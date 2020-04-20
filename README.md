# kafka-connect

## Getting Started

1. To get started you'll want to install Docker for your OS:
- https://hub.docker.com/editions/community/docker-ce-desktop-mac/
- https://hub.docker.com/editions/community/docker-ce-desktop-windows/
- https://runnable.com/docker/install-docker-on-linux

2. After Docker is installed and running on your machine you call pull this repo:
`git clone https://github.com/Onemata/kafka-connect.git`

3. From there if you're just playing or in development `docker-compose up --build` will build the container and start the kafka stack in your command line window so you can easily see the output as things connect and run.

## Background

We need Kafka Connect working standalone for connecting to Oracle Cloud and to run AWS Lambda's from our Kafka topics. 

We're starting from https://github.com/zenreach/docker-kafka-connect which is using Confluent's confluentinc/cp-kafka-connect:4.0.0

We want to add Confluent's Lambda Connector Sink: https://www.confluent.io/hub/confluentinc/kafka-connect-aws-lambda

And any Oracle Cloud Dependencies: 
- https://blogs.oracle.com/developers/migrate-your-kafka-workloads-to-oracle-cloud-streaming
- https://blogs.oracle.com/developers/using-kafka-connect-with-oracle-streaming-service-and-autonomous-db

Debezium has Kafka Connect setup as well minus the Lambda sink connector: https://hub.docker.com/r/debezium/connect

