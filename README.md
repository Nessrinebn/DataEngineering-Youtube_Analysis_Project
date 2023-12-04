#  YouTube Analysis Project - End- to-End Data Engineering utilizing AWS cloud and Python Project
# Overview:
This project is designed to securely handle, streamline, and analyze structured and semi- structured data from YouTube videos. It focuses on categorizing videos and assessing trending metrics to derive meaningful insights.
# Project Objectives:
1. Data Ingestion
2. ETL System
3. Data Lake Implementation
4. Scalability Assurance
5. Cloud Integration (AWS) 
6. Reporting Dashboards
# Services we will be using:
1. Amazon S3: Amazon S3 is an object storage service that provides manufacturing scalability, data availability, security, and performance. 
2. AWS IAM: This is nothing but identity and access management which enables us to manage access to AWS services and resources securely.
3. QuickSight: Amazon QuickSight is a scalable, serverless, embeddable, machine learning-powered business intelligence (BI) service built for the cloud.
4. AWS Glue: A serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development.
5. AWS Lambda: Lambda is a computing service that allows programmers to run code without creating or managing servers.
6. AWS Athena: Athena is an interactive query service for S3 in which there is no need to load data it stays in S3.
# Pipeline Phases:
The project unfolds in three key phases: 
1. Extract:
- Data extraction from Kaggle, featuring daily statistics of popular YouTube videos.
- AWS Lambda deployment for extraction function.
-  Automated extraction triggered by AWS CloudWatch at regular intervals.
-   Raw data stored in AWS S3 Bucket under "de-on-youtube-raw-ind-dev."
2. Transform:
 - S3 triggers activating a Lambda function for data transformation.
 - Categorized data by region, moved from "de-on-youtube-raw-ind-dev" to "de-on- youtube-cleansed-ind."
3. Load:
- Glue Crawler for schema inference upon new data addition.
- Amazon Athena renders the final dataset queryable and analyzable.
# Dataset Used:
This Kaggle dataset contains statistics (CSV files) on daily popular YouTube videos over the course of many months. There are up to 200 trending videos published every day for many locations. The data for each region is in its own file. The video title, channel title, publication time, tags, views, likes and dislikes, description, and comment count are among the items included in the data. A category_id field, which differs by area, is also included in the JSON file linked to the region.

https://www.kaggle.com/datasets/datasnaek/youtube-new

