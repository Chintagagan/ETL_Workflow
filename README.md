# ETL Pipeline with AWS Integration

# Project Overview
This ETL (Extract, Transform, Load) project is designed to ingest data in various formats (CSV, JSON, XML), transform it, and load it into an AWS RDS database. The project leverages AWS services, including S3 for data storage and Glue (optional) for automated data transformation. The pipeline performs data extraction, cleaning, unit conversions, and loading, with logging enabled to track each phase.

Prerequisites
Python 3.x: Required for running the ETL scripts
AWS Account: Access to AWS services like S3, RDS, and Glue
Required Python Libraries:
boto3: For interacting with AWS services (S3, RDS)
pandas: For data manipulation and transformation
sqlalchemy: For connecting and loading data into RDS
logging: For tracking and storing logs
