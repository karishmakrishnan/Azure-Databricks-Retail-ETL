📊 Azure Databricks Retail ETL Pipeline
Overview
This project implements an end-to-end data engineering pipeline using Azure Databricks and ADLS Gen2 following the Medallion Architecture.
Synthetic retail data is generated to simulate real-world application and CDC feeds, then processed through Bronze, Silver, and Gold layers using Apache Spark and Delta Lake.

Architecture
RAW (CSV in ADLS)
   ↓
BRONZE (Delta – schema enforced)
   ↓
SILVER (Delta – enriched, optimized joins)
   ↓
GOLD (Delta – analytics-ready)

Technologies Used
Azure Databricks
Apache Spark
Delta Lake
Azure Data Lake Storage Gen2

Key Engineering Concepts Applied
Broadcast joins for small dimension tables
Handling skewed data distributions
Adaptive Query Execution (AQE)
Partitioning strategies
Delta Lake ACID guarantees
Production-style storage layout

Highlights
Orders dataset intentionally skewed to simulate real workloads
Bronze layer enforces structure and reliability
Silver layer resolves column conflicts and optimizes joins
Gold layer provides business-ready aggregations

Authentication
For learning purposes, storage account access keys were used.
In production, Managed Identity or Service Principal would be used.
