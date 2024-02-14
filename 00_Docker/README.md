## 00_Docker_Practice

### Prerequisites  

* Install Docker Desktop (https://www.docker.com/products/docker-desktop/)  
_Once Docker is installed :_
* Pull a Python image, e.g. `docker pull python:3.12.2-slim-bookworm`
* Pull a Jupyter Pyspark image, e.g. `docker pull quay.io/jupyter/pyspark-notebook`

### Session walkthrough

##### 1) Poll

##### 2) Docker presentation

##### 3) Docker CLI

`docker run python:3.12-slim-bookworm`

Notes:
* Running with `-it` options to have an interactive TTY
* CLI reference: https://docs.docker.com/engine/reference/commandline/docker/
* DockerHub (https://hub.docker.com/) and other registries
* Review Python Dockerimage

##### 4) PySpark using Docker

Notes:
* Review compose.yml
* `docker compose up -d`
* Move the example.ipynb file to the `mnt` folder
* Review Jupyter UI, run the example notebook
* Review Spark UI

##### 5) Breakout session

Notes:
* Get to know some of your fellow students 
* Class assignment. You are free to use any resource (including ChatGPT and equivalents).  
  The only limitation is that you cannot use any other Python package besides PySpark.
* Read the `Thailand domestic tourism` parquet file into a Spark dataframe  
  Further info: https://www.kaggle.com/datasets/thaweewatboy/thailand-domestic-tourism-statistics
* Try to do exploratory data analysis on the dataframe
* Challenge: output an aggregation into a JSON file. 
  * The following columns are mandatory:
    * date | province_eng | no_percentage_of_foreign_tourists | revenue_percentage_of_foreign_tourists
  * no_percentage_of_foreign_tourists = no_tourist_foreign / no_tourist_all 
  * revenue_percentage_of_foreign_tourists = revenue_foreign / revenue_all  
* Group presentations and discussion.

##### 6) Review Databricks Community edition

Notes:  
* https://www.databricks.com/try-databricks
* Walkthrough of how to work with Databricks CE
* Discuss pros and cons of Databricks vs Docker vs local machine

##### 7) Quiz