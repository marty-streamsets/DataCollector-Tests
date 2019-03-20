# 04_Kafka_Read

## Description

This will test a read from Kafka.

## Instructions

- From SDC:
  - Import pipeline p900_TEST_04_Kafka_Read.json
  - Configure pipeline
    - Error Records
      - "Error Records" to Discard
    - Parameters
      - KAFKA_BROKER to <host>:<port>
      - KAFKA_ZOOKEEPER to <host>:<port>
      - KAFKA_CONSUMER_GROUP to streamsetsDataCollector
      - KAFKA_TOPIC to TEST_Kafka
    - Kafka Consumer
      - General
        - "Stage Library" to correct version
      - Kafka
        - "Auto Offset Reset" to Earliest
      - Data Format
        - "Data Format" to JSON
  - Validate/Preview/Run
