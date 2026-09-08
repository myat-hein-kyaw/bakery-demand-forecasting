# Bakery Demand Forecasting & Cloud Production Planning Framework

A machine learning project for bakery demand forecasting using PySpark, Apache Spark and AWS cloud architecture.

## Project Overview

This project analyses bakery operational data to forecast product demand and support production planning. It uses PySpark for large-scale data processing and compares multiple machine learning models for demand prediction.

The project also proposes an AWS-based cloud architecture for scalable data processing, analytics and reporting.

## Technologies Used

- Python
- PySpark
- Apache Spark
- Spark MLlib
- Machine Learning
- Google Colab
- AWS S3
- AWS Glue
- Amazon EMR
- Amazon Athena
- Amazon QuickSight

## Dataset & Scale

- Public bakery operational dataset
- Data covers 2019–2023
- 35 bakery branches
- 78 products
- 1,037,791 production-demand observations used for machine learning
- Chronological split: 2019–2022 for training and 2023 for testing

## Models & Results

The following forecasting approaches were compared:

- Mean Baseline
- Linear Regression
- Random Forest Regression
- Gradient Boosted Trees (GBT)

### Model Performance

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Mean Baseline | 45.69 | 29.27 | ~0.000 |
| Linear Regression | 44.19 | 28.40 | 0.0647 |
| Random Forest | 41.66 | 28.10 | 0.169 |
| Gradient Boosted Trees | 40.49 | 28.25 | 0.215 |

GBT achieved the best overall performance with the lowest RMSE and highest R², while Random Forest achieved the lowest MAE.

## Proposed AWS Architecture

The project proposes the following AWS-based workflow:

Bakery Branches → Amazon S3 (Raw Data) → AWS Glue ETL → AWS Glue Data Catalog → Amazon S3 (Curated Data) → Amazon EMR with PySpark → Forecast Results → Amazon Athena → Amazon QuickSight

### Security & Monitoring

- IAM for access control and least-privilege permissions
- AWS KMS for encryption key management
- S3 Block Public Access to prevent public exposure
- Private VPC networking for data processing
- AWS CloudTrail for audit logging
- Amazon CloudWatch for monitoring, logs and alerts
