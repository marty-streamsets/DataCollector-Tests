# 02_HDFS_Write

## Description

This will test a write to HDFS.

## Instructions

- From Hadoop Node OS:

  - Create the output directory if it doesn't exist

    ```bash
    sudo runuser -l hdfs -c "hdfs dfs -mkdir -p /data/taxidata/output"
    sudo runuser -l hdfs -c "hdfs dfs -chmod -R 777 /data/"
    ```

- From SDC:

  - Import pipeline p900_TEST_02_HDFS_Write.json
  - Configure pipeline
    - Error Records
      - "Error Records" to Discard
    - Dev Data Generator
      - Data Generator
        - "Fields to Generate"
          - KeyField	INTEGER
          - DataField	STRING
        - "Root Field Type" to LIST_MAP 
      - Hadoop FS
        - General
          - "Stage Library" to correct version
        - Hadoop FS
          - "Hadoop FS Configuration Directory" to /var/lib/sdc-resources/hadoop-conf
      - Output Files
        - "Files Prefix" to <blank>
        - "Directory Template" to /data/taxidata/output
      - Data Format
        - "Data Format" to Delimited
        - "Header Line" with Header Line
  - Validate/Preview/Run
