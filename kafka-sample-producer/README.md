# kafka-sample-producer

This is a Spring Boot sample application that makes use of the `kafka-connector` and Dingo Kakfa to bind to a Kafka service and produce messages.

## Using kafka-sample-producer

1. Git checkout and build the modules (if you have not already done so):

  ```bash
  git clone https://github.com/dingotiles/dingo-kafka-sample-apps.git
  cd dingo-kafka-sample-apps
  mvn -Dmaven.test.skip=true install
  ```

1. Deploy kafka-sample-producer. There is nothing to configure, other than maybe changing the name of the services in the manifest file, because the name should match the name you give to the kafka-service created.

  ```bash
  cd kafka-sample-producer
  cf push
  ```

2. Once the app has been pushed successfully and is running, tail the app logs using the following command:

  ```bash
  cf logs kafka-sample-producer
  ```  

3. The producer app will send messages every 10 seconds and the logs will reflect that. Look at the [README](https://github.com/dingotiles/dingo-kafka-sample-apps/tree/master/kafka-sample-consumer) for `kafka-sample-consumer` to set up an app to subscribe to the messages published by `kafka-sample-producer`. It will work as long as they are both bound to the _same_ kafka service instance.  
