## 01_HDFS_Practice

### Prerequisites  
* Pull the HDFS namenode and datanode images:  
`docker pull bde2020/hadoop-namenode:2.0.0-hadoop3.2.1-java8`  
`docker pull bde2020/hadoop-datanode:2.0.0-hadoop3.2.1-java8`

### Session walkthrough

##### 1) Poll

##### 2) Docker presentation

##### 3) Walkthrough

Original source: `https://github.com/big-data-europe/docker-hadoop`

Using the compose.yml in this repo, start the containers with `docker compose up -d`

Let's log into the namenode:
`docker exec -it namenode bash`  

CLI docs:  
https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-hdfs/HDFSCommands.html  
https://hadoop.apache.org/docs/current/hadoop-project-dist/hadoop-common/FileSystemShell.html  


Check the HDFS files:  
`hdfs dfs -ls /` 

Create a text file in the `tmp` folder on your local machine and add some words.  

Create a directory for hadoop input  
`hdfs dfs -mkdir -p /user/hadoop/{folder}`  

Put the text file into hadoop file system:  
`hdfs dfs -put file:/tmp/files/{file} hdfs:/user/hadoop/{folder}/`  

Check that the file exists:  
`hdfs dfs -ls /user/hadoop/{folder}`  

You can also check that the file exists from the Hadoop UI in your browser:  
`localhost:9870`  

You can make a file with single replication:  
`hdfs dfs -D dfs.replication=1 -put file:/tmp/files/{file} hdfs:/user/hadoop/{file_single}`

You can verify how the data is actually stored by going into the datanodes:  
`docker exec -it datanode1 bash`  
`cd /hadoop/dfs/data` and navigate down...

##### 4) Breakout session

Notes:
* Class assignment. You are free to use any resource (including ChatGPT and equivalents).  
* Extend the docker compose file to include the PySpark container from last time.
* Start the PySpark container
* Add the csv file from the following location to your `mnt` folder (for PySpark):  
https://gist.githubusercontent.com/tadast/8827699/raw/61b2107766d6fd51e2bd02d9f78f6be081340efc/countries_codes_and_coordinates.csv
* Read in the csv into a dataframe
* Export the csv into a parquet file on HDFS
* Group presentations and discussion.

##### 5) Quiz