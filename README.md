# Docker-based Hadoop / Spark clusters

Simplified version (no Hive) based on: https://github.com/big-data-europe/docker-hadoop-spark-workbench
Includes 3 workers to run on a single machine with no scale options. Some files could be unused (still not perfectly clean). 

## How to use deploy

```
    docker-compose up -d
```

# Interfaces

* Namenode: http://localhost:50070
* Datanode-1: http://localhost:50001
* Datanode-2: http://localhost:50002
* Datanode-3: http://localhost:50003
* Spark-master: http://localhost:8080
* Hue (HDFS Filebrowser): http://localhost:8088/home

# Important

When opening Hue, you might encounter ```NoReverseMatch: u'about' is not a registered namespace``` error after login. I disabled 'about' page (which is default one), because it caused docker container to hang. To access Hue when you have such an error, you need to append /home to your URI: ```http://docker-host-ip:8088/home```
