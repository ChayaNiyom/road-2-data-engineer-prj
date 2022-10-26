# Road to Data Engineer project
## Project from Road to Data Engineer course by DataTh

This project shows the basic concept of ETL, which stands for extract, transform, and load. It contain 
* **Data Collection**
* **Data Cleansing**
* Transport to **Data Lake**
* **Data Pipeline Orchestration**
* Transport to **Data Warehouse**
* **Data Visualisation**

The main cloud service they use in this project is Google Cloud Service. The database of this project comes from the creators of R2DE course.For Data Collection and Data Cleansing session, teachers let us use Google Colab as the notebook for coding.

### Data Collection
For data collection, we connect MySQL database through Python using PyMySQL Package. Before we connect to database, we need to config database credential (No code revealed here since it's the secret of the creator).
After that, we convert it to Pandas to make it easier for user and make the tables looks more beautiful. Then, we join the tables (audible_transaction & audible_data).
Not only a normal MySQL database, but teachers also show how to get data from REST API using Requests package.
Finally, we save the tables as CSV file for the further process.

### Data Cleansing
For data cleansing, we're going to clean and prepare the data before we transport the data to the Data Lake. In this cleansing process, we use Spark through Python using PySpark Package.
First, we set the environment for Python to let it recognise Spark. Next, we install PySpark into Python and load the data to Spark. Then, we do the data profiling to understand the several information of each columns, such as count, mean, standard deviation, min, and max. After that, we do a syntactical anomalies (such as correcting the spellings) , a sematic anomalies (such as correcting the outlier), and fill the null value. Finally, we save the cleaned data as CSV files for the further process.

### Data Lake
As I mentioned, we use Google Cloud Service as a main cloud service. So for data lake, we use Google Cloud Storage for keeping the data we previously did. 
To upload the data we had to the Cloud Storage, we need to create the bucket. Bucket in Cloud Storage is similar to the folder in our computer, but for bucket, we can transport the data to the data warehouse that support Google Cloud Storage

### Data Pipeline Orchestration
Apache Airflow is the tool they selected for this project since Airflow is easy to monitor and run automatically. To use Airflow for this project, we need to active the service called Google Cloud Composer. Google Cloud Composer allows us to create the environment for Airflow and able to use Airflow without additional investment on server.
