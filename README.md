
# GHG Twitter Messaging Tracker - Apache Kafka repository

## 1) How to Install

```docker-compose up -d```


## 2) How to create topics

- Access kafka service
  
    ```docker exec -it ghg-twitter-kafka_kafka_1 /bin/bash```
###
- Check for kafka scripts location
    ```which kafka-topics.sh```
###
- Create a new topic
    ```kafka-topics.sh --create --topic twitter.programming --replication-factor 1 --partitions 2 --bootstrap-server localhost:9092```

## 3) How to list existing topics

- Inside docker service
    ```kafka-topics.sh --list --bootstrap-server=localhost:9092```
