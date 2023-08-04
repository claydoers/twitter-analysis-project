# Twitter Data Pipeline Project

## Overview
This goal of this project was to securely ingest, streamline and perform analysis on raw data from Twitter using the Twitter API and further transform the data using an ETL process.

## Goals
<li>Data Ingestion</li>
<li>ETL</li>
<li>Data Lake</li>
<li>Automation</li>
<li>Cloud Processing</li>

## Tools used
<li>Twitter API - How the data is accessed</li>
<li>Amazon S3 - Data lake/Object storage</li>
<li>Amazon EC2  - Cloud computing service to process our code so we arent processing it locally.</li>
<li>Apache Airflow - Workflow orchestration.</li>
<li>Python/Pandas - ETL/data transformation</li>

## Simple Architectual Diagram
![image](https://github.com/claydoers/de-twitter-analysis-project/assets/109707159/1f721c81-d340-4cef-abe0-55700c172bcb)

## Automated Pipeline
This data pipeline is designed to run daily. The Airflow DAG is responsible for triggering the python script (twitter_etl.py). This ensures that the latest data from the Twitter API is fetched regularly. 

Upon successful extraction the ETL process is triggered for specified Twitter user. The data is transformed from JSON format to CSV using a Pandas Dataframe and then the object (CSV) is uploaded to the data lake (AWS S3). 

The transformed data can then be accessed using a visualization tool such as Tablaeu, Quicksight, Power BI, or Superset to build dashboards to conduct various types of analysis. 

## Conclusion
The purpose of this project was to utilize the Twitter API, AWS services, and Airflow to create an automated data pipeline that can efficiently process user/tweet data to be made available for analysis. This project showcases the versatility of AWS service in building robust and automated DE solutions. 



