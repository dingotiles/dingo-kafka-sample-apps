# Sample applications for Dingo Kafka

Dingo Kafka is a distribution of Apache Kafka for Pivotal Cloud Foundry.

This repository contains sample applications: a producer of events to a Kafka topic, and a consumer of events from the same Kafka topic.

The instructions assume that you are deploying to Pivotal Cloud Foundry with Dingo Kafka already installed by your platform operator.

## Preparation

```bash
git clone https://github.com/dingotiles/dingo-kafka-sample-apps.git
cd dingo-kafka-sample-apps
mvn -Dmaven.test.skip=true install
```

## Sub-projects

This project includes the following modules. See their respective READMEs for more information.

### [kafka-connector](https://github.com/dingotiles/dingo-kafka-sample-apps/tree/master/kafka-connector)
* This module contains spring-cloud-connector code that can optionally be used by consumers of the brokered service, to make it easier to connect to the Dingo Kafka back-end services.

### [kafka-sample-consumer](https://github.com/dingotiles/dingo-kafka-sample-apps/tree/master/kafka-sample-consumer)
* A sample project that can be used to demo message consumption, and illustrates the use of the broker-connector.

### [kafka-sample-producer](https://github.com/dingotiles/dingo-kafka-sample-apps/tree/master/kafka-sample-producer)
* A sample project that can be used to demo message production, and illustrates the use of the broker-connector.

## Credits

These sample applications were first published by Pivotal https://github.com/cf-platform-eng/kafka-service-broker

This repository was created as a clean project primarily because https://github.com/cf-platform-eng/kafka-service-broker was a huge repository and very slow to download over small internets. Apologies for confusion.
