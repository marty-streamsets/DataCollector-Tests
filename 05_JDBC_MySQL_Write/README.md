# 05_JDBC_MySQL_Write

## Description

This will test a write to JDBC (MySQL).

## Instructions

- From SDC:
  - Import pipeline p900_TEST_05_JDBC_MySQL_Write.json
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
    - JDBC Producer
      - JDBC
        - JDBC Connection String to "Broker URI" to jdbc:mysql://marty-1:3306/demo
        - Use Credentials to "checked"
        - Table Name to "test_jdbc"
      - Credentials
        - Username to <mysql username>
        - Password to <mysql password>
  - Validate/Preview/Run
