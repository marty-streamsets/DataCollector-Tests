# 05_JDBC_MySQL_Write

## Description

This will test a write to JDBC (MySQL).

## Instructions

- **From MySQL**
  - If needed, execute `create_table.sql` to create the target table
- From SDC:
  - Import pipeline *p900_TEST_05_JDBC_MySQL_Write.json*
  - Configure pipeline
    - Pipeline
      - Error Records
        - Error Records to `Discard`
      - Parameters
        - JDBC_Connection_String to `jdbc:mysql://marty-1:3306/demo`
        - Table_Name to `test_jdbc`
    - Dev Data Generator
      - Data Generator
        - Fields to Generate
          - `KeyField	INTEGER`
          - `DataField	STRING`
        - Root Field Type to `LIST_MAP`
        - Batch Size to `1`
    - JDBC Producer
      - JDBC
        - Use Credentials to `checked`
      - Credentials
        - Username to `<mysql-username>`
        - Password to `${runtime:loadResource("JDBCpassword.txt", true)}`
  - Validate/Preview/Run
