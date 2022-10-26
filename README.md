# Road to Data Engineer project
## Project from Road to Data Engineer course by DataTh

This project shows the basic concept of ETL, which stands for extract, transform, and load. It contain 
* **Data Collection**
* **Data Cleansing**
* Transport to **Data Lake**
* **Data Pipeline Ochestrarion**
* Transport to **Data Warehouse**
* **Data Visualisation**

The main cloud service they use in this project is Google Cloud Service. The database of this project comes from the creators of R2DE course.

### Data Collection
For data collection, we connect MySQL database through Python using PyMySQL Package. Before they connect to database, we need to config database credential (No code revealed here since it's the secret of the creator).
After that, we convert it to Pandas to make it easier for user and make the tables looks more beautiful. Then, we join the tables (audible_transaction & audible_data).
Not only a normal MySQL database, but they also show how to get data from REST API using Requests package.
Finally, they save the tables as CSV file for the further process.
