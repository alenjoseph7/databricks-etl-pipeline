# Databricks ETL Pipeline with Delta Lake

## Overview
This project implements an end-to-end ETL pipeline using Databricks, PySpark, and Delta Lake.
The pipeline follows the Bronze–Silver–Gold architecture to transform raw data into analytics-ready datasets.

## Architecture
Bronze → Silver → Gold

- **Bronze (taxi_data)**: Raw taxi trip data ingested into a Delta table
- **Silver (silver_taxi)**: Cleaned and validated data with enforced schema and data quality rules
- **Gold (gold_taxi_metrics, gold_taxi_daily_metrics)**: Aggregated business metrics for analytics and reporting

## Technologies Used
- Databricks (Free Edition)
- PySpark
- Delta Lake
- Spark SQL

## ETL Workflow
1. Ingest raw CSV data into Databricks and persist as a Bronze Delta table
2. Clean and transform data in the Silver layer:
   - Timestamp normalization
   - Null handling
   - Data validation and filtering
3. Aggregate data into Gold tables for business analytics:
   - Total trips
   - Average fare and trip distance
   - Daily revenue
   - Average trip duration

## Data Quality Checks
- Validation of timestamps
- Removal of invalid distances and fares
- Handling missing passenger counts

## Outcome
The pipeline produces reliable, analytics-ready datasets suitable for dashboards, reporting, and downstream machine learning workflows.

## How to Run
The pipeline is implemented as a Databricks notebook and can be executed sequentially from ingestion through analytics layers within the Databricks workspace.
