# 04_Kafka_Read

## Description

This will test a read from Kafka.

## Instructions

- From SDC:
  - Import pipeline p900_TEST_03_Kafka_Read.json
  - Configure pipeline
    - Error Records
      - "Error Records" to Discard
    - Kafka Consumer
      - General
        - "Stage Library" to correct version
      - Kafka
        - "Broker URI" to <broker>:<port>
        - "Zookeeper URI" to <broker>:<port>
        - "Consumer Group" to streamsetsDataCollector
        - "Topic" to TEST_Kafka
        - "Auto Offset Reset" to Earliest
        - "Kafka Configuration" to auto.offset.reset = earliest
      - Data Format
        - "Data Format" to JSON
  - Validate/Preview/Run
