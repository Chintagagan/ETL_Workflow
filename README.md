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
