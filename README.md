## Yelp Business Review Data Pipeline

## Overview

The Yelp Business Review Data Pipeline is a comprehensive solution for processing and analyzing Yelp business review data. This end-to-end data pipeline integrates various technologies, including Python, Kafka, AWS services (DynamoDB, S3, Redshift), PySpark, AWS Lambda, and Power BI. The project enables real-time streaming, change data capture (CDC), daily batch processing, and data visualization to gain insights into customer sentiment, business performance, and industry trends.

##   Project Pipeline
![image](https://github.com/YMMSSH/Business_Reviews_Pipeline/assets/55538499/e8ebb426-2fca-4f7c-a8f0-e97696c5463f)


## Technology Stack

Python
Kafka
AWS services (DynamoDB, S3, Redshift)
PySpark
AWS Lambda
Power BI
Introduction
Our big data project revolves around processing and analyzing Yelp business review data. The pipeline handles real-time streaming, CDC, daily batch processing, and data visualization. The key data sources include three main tables from Yelp's dataset: Business, Reviews, and Users, providing valuable information about businesses, customer reviews, and user details.

## Key Components

## Kafka on Premise

Used for real-time data streaming.
Producers ingest data from JSON and CSV files.
Topics created for each table (Business, Reviews, Users) for organized data streams.

## Python Producers

Python scripts serve as producers for streaming data into Kafka topics.
Continuous ingestion of Yelp dataset into the Kafka cluster.

## PySpark Consumer

Implemented using PySpark to process and transform incoming data from Kafka.
Enriches data and prepares it for storage in DynamoDB.

## DynamoDB

NoSQL database for real-time storage of processed Yelp data.
AWS Lambda Triggers in DynamoDB configured for CDC processes.

## AWS Lambda Triggers

Functions trigger CDC processes in DynamoDB on data changes.
Captures and propagates changes to an S3 bucket for daily batch processing.

## S3 Batch Processing

Daily batch processing on data stored in S3 for aggregation, cleaning, and transformation.
Processed data made ready for loading into the Redshift data warehouse.

## Redshift Data Warehouse

Central data warehouse for storing Yelp data in a structured and optimized format.
Daily batches of processed data from S3 loaded for analytical queries.

## Power BI Dashboard

Utilized for data visualization, creating interactive dashboards and reports.
Direct queries to Redshift for real-time visualization and analysis.

## Workflow

## Real-time Streaming

Yelp data continuously streamed in real-time from JSON and CSV files into Kafka topics.

## PySpark Data Processing

PySpark jobs in the Kafka consumer process and transform incoming data before uploading it to DynamoDB.

## Change Data Capture (CDC)

AWS Lambda Triggers in DynamoDB capture changes in real-time, ensuring data consistency.

## S3 Batch Processing

Daily batches of data from DynamoDB processed and transformed in S3 for optimal analytics.

## Redshift Data Loading

Processed data loaded daily into Redshift for historical and analytical queries.

## Power BI Data Visualization

Power BI connected to Redshift for real-time queries, enabling the creation of interactive dashboards and reports.

## Benefits

## Real-time Data Insights

Leveraged Kafka and PySpark for real-time data streaming and processing, providing immediate insights into Yelp data.

## Scalable and Flexible

AWS services (DynamoDB, S3, Redshift) offered scalability and flexibility to handle growing data volumes and analytical needs.

## Change Data Capture

Implemented CDC in DynamoDB using Lambda Triggers for capturing and propagating real-time data changes.

## Daily Batch Processing

Utilized S3 for efficient daily batch processing, ensuring data is optimized for Redshift.

## Data Visualization

Power BI employed for creating visually appealing and interactive dashboards for easy data exploration and analysis.
