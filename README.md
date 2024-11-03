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


<h2>Step 2: AWS Setup</h2>

1.Create an S3 Bucket
Set up a new S3 bucket  to store both raw and transformed data files.

2.Set Up AWS RDS
