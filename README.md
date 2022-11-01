# Road to Data Engineer project
## Project from Road to Data Engineer course by DataTh

This project shows the basic concept of ETL, which stands for extract, transform, and load. It contains 6 workshops, which are
* **Data Collection**
* **Data Cleansing**
* **Data Lake**
* **Data Pipeline Orchestration**
* **Data Warehouse**
* **Data Visualisation**

Google Cloud Service is the primary cloud service they utilize for their project. The authors of the R2DE course provided the database for this project. Teachers allowed us to use Google Colab as the coding notebook for the sessions on data collection and data cleaning.

### Workshop 1: Data Collection
We used PyMySQL Package to connect the MySQL database to Python for the purpose of data collection. Before connecting to the database, we had to configure the database credentials (the creator-only code is not shown here).
Then, in order to make it simpler for users and improve the aesthetics of the tables, we changed it to Pandas. The tables (audible transaction & audible data) were then connected.
Teachers demonstrated how to use the Requests package to obtain data from REST APIs in addition to a standard MySQL database.
Finally, We saved the tables as a CSV file for use in the following steps.

### Workshop 2: Data Cleansing
For data cleansing, we're going to clean and prepare the data before we transport the data to the Data Lake. In this cleansing process, we use Spark through Python using PySpark Package.
First, we set the environment for Python to let it recognise Spark. Next, we install PySpark into Python and load the data to Spark. Then, we did the data profiling to understand the several information of each columns, such as count, mean, standard deviation, min, and max. After that, we did a syntactical anomalies (such as correcting the spellings), a sematic anomalies (such as correcting the outlier), and fill the null value. Finally, we saved the cleaned data as CSV files for the further process.

### Workshop 3: Data Lake
As I mentioned, we use Google Cloud Service as a main cloud service. So for data lake, we use Google Cloud Storage for keeping the data we previously did. 
To upload the data we had to the Cloud Storage, we need to create the bucket. Bucket in Cloud Storage is similar to the folder in our computer, but for bucket, we can transport the data to the data warehouse that support Google Cloud Storage

### Workshop 4: Data Pipeline Orchestration
Apache Airflow is the tool they selected on this orchestration workshop since Airflow is easy to monitor and run automatically. To use Airflow for this project, we need to active the service called Google Cloud Composer. Google Cloud Composer allows us to create the environment for Airflow and able to use Airflow without additional investment on server. DAG, or Directed Acyclic Graph, is a topic we studied in this workshop. DAG would give the direction of the task for the data, or data flow. To run automatically, we need Cron as a schedule interval. Cron allow us to schedule Airflow as the users want.

### Workshop 5: Data Warehouse
Data warehouse is the place where the data need to be ready for data scientist or data analyst use for their purposes. Google BigQuery is one of the tools we use from Google Cloud Service. In this workshop, we basically learned how to link Google Cloud Storage and Google BigQuery using Apache Airflow and write the DAG to merge the data from Database (MySQL) to REST API. We tried some queries on the merged data to see that it worked or not.

### Workshop 6: Data Visualisation 
Data visualisation is how we’re going to visualise the data we have to a dashboard that can explain the status of the data. In this workshop, we use Google Data Studio as our main instrument. Before we begin, we must connect Google Data Studio to the data warehouse. Then we did some visualise according to the examples of the wireframes from Business Analyst.
