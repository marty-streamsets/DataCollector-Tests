# 01_HDFS_Read

#### Description

------

This will test a read from HDFS.

#### Instructions

------

- From Hadoop Node OS:

  - Move the file: nyc_taxi_data.csv to HDFS (/data/taxidata)

    - Create the directory if it doesn't exist

    ```bash
    sudo runuser -l hdfs -c "hdfs dfs -mkdir /data"
    sudo runuser -l hdfs -c "hdfs dfs -mkdir /data/taxidata"
    sudo runuser -l hdfs -c "hdfs dfs -chmod -R 777 /data/"
    ```

    - Put the file in above directory using HUE or "hdfs dfs -put" command

- From SDC:

  - Import pipeline
  - Configure pipeline



