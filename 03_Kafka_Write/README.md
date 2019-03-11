# 03_Kafka_Write

## Description

This will test a write to Kafka.

## Instructions

- From SDC:
  - Import pipeline p900_TEST_03_Kafka_Write.json
  - Configure pipeline
    - Error Records
      - "Error Records" to Discard
    - Dev Data Generator
      - Data Generator
        - "Fields to Generate"
          - KeyField	INTEGER
          - DataField	STRING
        - "Root Field Type" to LIST_MAP 
        - "Batch Size" to 1
    - Kafka Producer
      - General
        - "Stage Library" to correct version
      - Kafka
        - "Broker URI" to <broker>:<port>
        - "Topic" to TEST_Kafka
      - Data Format
        - "Data Format" to JSON
  - Validate/Preview/Run
