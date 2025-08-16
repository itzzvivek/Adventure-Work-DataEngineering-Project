#Azure Data Engineering Project

A complete end-to-end Azure Data Engineering pipeline using the medallion architecture: Bronze → Silver → Gold. The project simulates a real-world data analytics solution using Azure services.

##Dataset

- **Source**: [AdventureWorks Dataset](https://www.kaggle.com/datasets/ukveteran/adventure-works)
- The dataset was pushed to GitHub and ingested into Azure Data Lake Storage Gen2 using Azure Data Factory.

##Tools & Technologies

- **Azure Data Factory** – Ingestion & pipeline orchestration  
- **Azure Data Lake Gen2** – Centralized data lake storage  
- **Azure Databricks** – Data transformation using PySpark  
- **Azure Synapse Analytics** – Analytical querying and reporting  
- **Power BI** – Data visualization (optional)

##Project Architecture

1. **Bronze Layer**  
   Raw data ingested from GitHub to Azure Data Lake using ADF pipelines. Dynamic parameters were configured using JSON files with GitHub URLs.

2. **Silver Layer**  
   Cleaned and transformed data using Azure Databricks with PySpark, stored as Parquet files.

3. **Gold Layer**  
   Processed and aggregated data ready for analytics. Connected to Synapse Analytics using external tables and made available for reporting.

##Key Features

- Parameterized ingestion using ADF’s `Copy Data`, `ForEach`, and `Lookup` activities  
- Managed identities and secure data access  
- Structured storage layer using the Medallion architecture  
- Scalable transformation using Databricks notebooks  
- Reporting-ready data exposed via Synapse Analytics

##Project Structure



![Screenshot (25)](https://github.com/user-attachments/assets/1f1f48ff-c117-42f7-9e44-2a825a508c4b)
