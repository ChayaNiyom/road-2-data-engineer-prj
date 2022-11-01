# Road to Data Engineer project
## Project from Road to Data Engineer course by DataTH


This project shows the basic concept of ETL, which stands for extract, transform, and load. It contains 6 workshops, which are

* **Data Collection**
* **Data Cleansing**
* **Data Lake**
* **Data Pipeline Orchestration**
* **Data Warehouse**
* **Data Visualisation**


Google Cloud Service is the primary cloud service they utilize for their project. The authors of the R2DE course provided the database for this project. Teachers allowed us to use Google Colab as the coding notebook for the sessions on data collection and data cleansing.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/ETL.jpg"/>
</p>

<h5 align="center"> Parts of Data Pipeline which are Extract, Transform, and Load (Credit: Road to Data Engineer 2.0 by DataTH) </h5>

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Overall_Workshop.jpg"/>
</p>

<h5 align="center"> Overview of Google Cloud Service tools we use in this workshop (Credit: Road to Data Engineer 2.0 by DataTH) </h5>

---

### Workshop 1: Data Collection
We used PyMySQL Package to connect the MySQL database to Python for the purpose of data collection. Before connecting to the database, we had to configure the database credentials (the creator-only code is not shown here).
Then, in order to make it simpler for users and improve the aesthetics of the tables, we changed it to Pandas. The tables (audible transaction & audible data) were then connected.
Teachers demonstrated how to use the Requests package to obtain data from REST APIs in addition to a standard MySQL database.
Finally, We saved the tables as a CSV file for use in the following steps.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop1_Description.jpg"/>
</p>

<h5 align="center"> Overview of Workshop 1 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---

### Workshop 2: Data Cleansing
Before transferring the data to the Data Lake, we will clean and prepare it as part of data cleansing. Using Python's PySpark package, we apply Spark in this cleaning process.
We first prepare Python's environment such that it can recognize Spark. The data is then loaded into Spark after PySpark has been installed in Python. Then, we profiled the data to understand the various details of each column, including the count, mean, standard deviation, minimum and maximum. After that, we completed a sematic anomalies (such as rectifying the outlier) and a syntactical abnormalities (such as filling the null value). Finally, for use in the following procedure, we saved the cleansed data as CSV files.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop2_Description.jpg"/>
</p>

<h5 align="center"> Overview of Workshop 2 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---

### Workshop 3: Data Lake
We use Google Cloud Provider as our primary cloud service, as I have indicated. In order to save the data we previously processed, we use Google Cloud Storage for the data lake. 
We must first create the bucket in order to upload the data we already had to the cloud storage. Comparable to a folder on a computer, a bucket in cloud storage allows us to send data to a data warehouse that supports Google Cloud Storage.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop3_Description.jpg"/>
</p>

<h5 align="center"> Overview of Workshop 3 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---

### Workshop 4: Data Pipeline Orchestration
Since Apache Airflow is simple to monitor and operate automatically, that is the tool they chose for this orchestration workshop. We must turn on the Google Cloud Composer service in order to use Airflow for this project. We can set up an environment for Airflow using Google Cloud Composer, and we can use Airflow without having to invest more money on servers. We covered the subject of DAG, or Directed Acyclic Graph, in this session. DAG would indicate the task's or data flow's direction. We require Cron as a schedule interval so that it can run automatically. We can schedule Airflow using Cron as the users see fit.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop4_Description.jpg"/>
</p>

<h5 align="center"> Overview of Workshop 4 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---

### Workshop 5: Data Warehouse
The data must be prepared in a data warehouse so that data scientists and analysts can use it for their objectives. One of the Google Cloud Service products we employ is Google BigQuery. In this workshop, we primarily learnt how to use Apache Airflow to connect Google Cloud Storage and Google BigQuery, as well as how to create a DAG to combine data from a database (MySQL) with a REST API. To test whether the merged data would function, we ran various queries on it.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop5_Description.jpg"/>
</p>

<h5 align="center"> Overview of Workshop 5 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---

### Workshop 6: Data Visualisation 
Data visualization is the method we'll use to translate the data we already have into a dashboard that can describe the data's state. Our primary tool in this workshop is Google Data Studio. Connecting Google Data Studio to the data warehouse is necessary before we start. Then, using Business Analyst's wireframe examples as a guide, we did some visualizing.

<p align="center">
<img src="https://github.com/ChayaNiyom/road-2-data-engineer-prj/blob/main/Workshop6_Wireframe.jpg"/>
</p>

<h5 align="center"> Overview of Wireframes we need to visualise in Workshop 6 (Credit: Road to Data Engineer 2.0 by DataTH) </h5>


---
