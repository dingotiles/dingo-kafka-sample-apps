# kafka-sample-consumer

This is a Spring Boot sample application that makes use of the `kafka-connector` and Dingo Kakfa to bind to a Kafka service and consume messages.

## Using kafka-sample-consumer
1. Git checkout and build the modules (if you have not already done so):

  ```bash
  git clone https://github.com/dingotiles/dingo-kafka-sample-apps.git
  cd dingo-kafka-sample-apps
  mvn -Dmaven.test.skip=true install
  ```

1. Deploy kafka-sample-consumer. There is nothing to configure, other than maybe changing the name of the services in the manifest file, because the name should match the name you give to the kafka-service created.

  ```bash
  cd kafka-sample-consumer
  cf push
  ```

2. Once the app has been pushed successfully and is running, tail the app logs using the following command:

  ```bash
  cf logs kafka-sample-consumer
  ```  

3. The consumer app will display any messages sent from the kafka-sample-producer (or any other app publishing to the kafka-service-instance) as long as they are both bound to the _same_ kafka service instance.  
