# 02_HDFS_Write

## Description

This will test a write to HDFS.

## Instructions

- **From Hadoop Node OS:**

  - Create the output directory if it doesn't exist

    ```bash
    sudo runuser -l hdfs -c "hdfs dfs -mkdir -p /data/taxidata/output"
    sudo runuser -l hdfs -c "hdfs dfs -chmod -R 777 /data/"
    ```

- **From SDC:**

  - Import pipeline *p900_TEST_02_HDFS_Write.json*
  - Configure pipeline
    - Error Records
      - Error Records to `Discard`
    - Parameters
      - HADOOP_FS_CONF_DIRECTORY to `/var/lib/sdc-resources/hadoop-conf`
      - FILES_PREFIX <blank>
      - DIRECTORY_TEMPLATE to `/data/taxidata/output`
    - Dev Data Generator
      - Data Generator
        - Fields to Generate
          - `KeyField	INTEGER`
          - `DataField	STRING`
        - Root Field Type to `LIST_MAP` 
      - Hadoop FS
        - General
          - Stage Library to *correct version*
      - Data Format
        - Data Format to `Delimited`
        - Header Line to `with Header Line`
  - Validate/Preview/Run
