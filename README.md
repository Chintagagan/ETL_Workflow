# ETL Pipeline with AWS Integration

# Project Overview
This ETL (Extract, Transform, Load) project is designed to ingest data in various formats (CSV, JSON, XML), transform it, and load it into an AWS RDS database. The project leverages AWS services, including S3 for data storage and Glue (optional) for automated data transformation. The pipeline performs data extraction, cleaning, unit conversions, and loading, with logging enabled to track each phase.

# Prerequisites
1.Python 3.x: Required for running the ETL scripts

2.AWS Account: Access to AWS services like S3, RDS, and Glue

3.Required Python Libraries:

4.boto3: For interacting with AWS services (S3, RDS)

5.pandas: For data manipulation and transformation

6.sqlalchemy: For connecting and loading data into RDS

7.logging: For tracking and storing logs


---------------------------------------------------------------------------

── README.md                  # Project documentation

── data/                      # Contains the raw data files (CSV, JSON, XML)

── logs/                      # Directory for log files

── etl_script.py              # Main ETL script

── transformed_data/          # Folder for transformed CSV files

---------------------------------------------------------------------------

# Steps to Run the ETL Pipeline

<h2> Step 1: Gather Data Files </h2>
1.Open a terminal and download the dataset using wget

wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0221EN-SkillsNetwork/labs/module%206/Lab%20-%20Extract%20Transform%20Load/data/source.zip


2. Unzip the downloaded file
unzip source.zip -d ./data/

<h2>2.Set Up AWS RDS</h2>
  - Create an RDS instance (MySQL or PostgreSQL) to store the transformed data.

  - Configure the security groups to allow access from your local machine or AWS Lambda functions.


<h2>Step 2: AWS Setup</h2>

1.Create an S3 Bucket
Set up a new S3 bucket  to store both raw and transformed data files.

2.Set Up AWS RDS

 - Create an RDS instance (MySQL or PostgreSQL) to store the transformed data.
 - Configure the security groups to allow access from your local machine or AWS Lambda functions.


<h2>Step 3: Import Libraries and Configure AWS Resources</h2>

- Import boto3, pandas, sqlalchemy, and logging in your ETL script.
- Set up AWS credentials and connection details in your environment variables or AWS configuration files to securely access S3 and RDS.

<h2>Step 4: Define Functions for ETL with AWS Integration</h2>

<h3>Extract Data</h3>

 - Upload raw CSV, JSON, and XML files to the S3 bucket.
 - Download files from S3 for further processing.

<h3>Transform Data</h3>

 - Clean and standardize data, performing necessary unit conversions (e.g., inches to meters, pounds to kilograms).

<h3>Load Data to AWS</h3>

 - Store the transformed CSV file in S3 (e.g., my-etl-project-bucket/transformed_data.csv).
 - Load data into the RDS database by connecting with sqlalchemy and using pandas to write data into a relational table.


