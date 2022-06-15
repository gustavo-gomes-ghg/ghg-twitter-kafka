
# GHG Twitter Messaging Tracker - Apache Kafka repository

## 1) How to Install

```
docker-compose up -d
```

## 2) How to create topics

- Access kafka service
  
    ```
    docker exec -it ghg-twitter-kafka_kafka_1 /bin/bash
    ```

- Check for kafka scripts location
    ```
    which kafka-topics.sh
    ```

- Create a new topic
    ```
    kafka-topics.sh --create --topic twitter.programming --replication-factor 1 --partitions 2 --bootstrap-server localhost:9092
    ```

## 3) How to list existing topics

- Inside docker service
    ```
    kafka-topics.sh --list --bootstrap-server=localhost:9092
    ```


# Zookeeper

## How to list the brokers
- Access the zookeeper service
    ```
    docker exec -it ghg-twitter-kafka_zookeeper_1 /bin/bash
    ```
###
- Access the zookeeper CLI, located on folder /opt/bitnami/zookeeper/bin/zkCli.sh
    ```
    /opt/bitnami/zookeeper/bin/zkCli.sh -server localhost:2181
    ```
###
- Explore the commands below
    ```
   ls # Gives the list of all properties to explore
   ls /brokers/ids # Gives the list of active brokers
   ls /brokers/topics #Gives the list of topics
   get /brokers/ids/0 #Gives more detailed information of the broker id '0'
   ```
