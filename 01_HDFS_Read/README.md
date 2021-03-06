# 01_HDFS_Read

## Description

This will test a read from HDFS.

## Instructions

- **From Hadoop Node OS:**

  - Move the file: *nyc_taxi_data.csv* to HDFS (`/data/taxidata`)

    - Create the directory if it doesn't exist

    ```bash
    sudo runuser -l hdfs -c "hdfs dfs -mkdir /data"
    sudo runuser -l hdfs -c "hdfs dfs -mkdir /data/taxidata"
    sudo runuser -l hdfs -c "hdfs dfs -chmod -R 777 /data/"
    ```

    - Put the file in above directory using HUE or "`hdfs dfs -put`" command

- **From SDC:**

  - Import pipeline *p900_TEST_01_HDFS Read.json*
  - Configure pipeline
    - Pipeline
      - Error Records
        - Error Records to `Discard`
      - Parameters
        - HADOOP_FS_CONF_DIRECTORY to `/var/lib/sdc-resources/hadoop-conf`
        - FILES_DIRECTORY to `/data/taxidata`
        - FILE_NAME_PATTERN to `*.csv`
    - Hadoop FS Standalone
      - General
        - Stage Library to *correct version*
      - Data Format
        - Data Format to `Delimited`
        - Header Line with `Header Line`
  - Validate/Preview/Run
