# Adventure Work - Azure Data Engineering Project

Creating an end-to-end Data Engineering pipeline from an API source to Azure Data Lake using a medallion architecture. This project involves transforming raw data into clean, structured datasets ready for client usage, leveraging Azure Synapse Analytics for final analytics and reporting.

## 🚀 Project Overview

This project is designed to demonstrate a comprehensive data engineering solution using Azure's cloud services. It follows the medallion architecture, which involves three distinct layers:

1. **Bronze (Raw Data)**: Stores raw data from the API.
2. **Silver (Cleaned Data)**: Data is cleaned and transformed.
3. **Gold (Aggregated Data)**: Final processed data, ready for analytics and client reporting.

The pipeline integrates various Azure services to ensure efficient data ingestion, transformation, and analytics.

## 🛠️ Technologies Used

- **Azure Resource Group**: Centralized management for all Azure resources used in the project.
- **Azure Data Lake Storage Gen2**: Acts as the primary storage layer, following the medallion architecture with containers for Bronze, Silver, and Gold layers.
- **Azure Data Factory (ADF)**:
  - **Linked Services**: Configured for connecting to the source (API) and the sink (Azure Data Lake).
  - **Activities Used**:
    - **Copy Data**: For ingesting data from the API into the Azure Data Lake (Bronze layer).
    - **Lookup**: Retrieves metadata or configuration information to drive dynamic pipeline execution.
    - **ForEach**: Handles iteration over multiple datasets or configurations for scalable data loading.
- **Azure Databricks**:
  - **MS Entra ID Integration**: Ensures secure access using Azure Active Directory (AAD).
  - **PySpark for Transformation**: Scripts written in PySpark to clean, filter, and transform data from the Silver to Gold layer.
- **Azure Synapse Analytics**:
  - **Serverless SQL Pool**: Used for querying data efficiently without provisioning dedicated compute resources.
  - **CETAS (CREATE EXTERNAL TABLE AS SELECT)**: Creates external tables from the transformed data in the Gold layer, enabling seamless querying and reporting.
- **Security**: Implemented using Azure Active Directory and access control policies to ensure data security across all services.

1. **Azure Services Setup**:
   - Create an Azure Resource Group and deploy the necessary services (Data Lake, Data Factory, Databricks, Synapse Analytics).
   - Set up Azure Data Lake Storage with containers for Bronze, Silver, and Gold layers.
   - Configure Azure Data Factory with linked services for the API source and Azure Data Lake sink.

2. **Databricks Setup**:
   - Launch Azure Databricks and create a cluster.
   - Import notebooks from the `notebooks/` directory and attach them to the cluster.
   - Ensure MS Entra ID access is configured for secure connectivity.

3. **Execute Pipelines**:
   - Run the Azure Data Factory pipeline to ingest data from the API to the Bronze layer.
   - Use Databricks notebooks to perform transformations and load data into the Silver and Gold layers.
   - Query the final datasets using Azure Synapse Analytics.

## 🛠️ Usage

- Use **Azure Data Factory** to trigger the pipeline for data ingestion from the API.
- Open **Databricks notebooks** and run the PySpark scripts for data transformation from Bronze to Silver and then to Gold.
- Query the cleaned and transformed data using **Azure Synapse Analytics**, leveraging serverless SQL pools for efficient querying.

## 🌟 Features

- **End-to-End Data Pipeline**: Automates the entire process from data ingestion to transformation and analytics.
- **Dynamic Pipelines**: Utilizes dynamic activities like **ForEach** and **Lookup** in Azure Data Factory for scalable data processing.
- **Secure Access**: Implements MS Entra ID for secure access to Azure Databricks and other services.
- **Medallion Architecture**: Follows a structured approach with Bronze, Silver, and Gold layers for efficient data organization.
- **Serverless Querying**: Leverages serverless SQL pools in Azure Synapse Analytics for cost-effective and scalable data querying.

## 📞 Contact

- **LinkedIn**: [Mohamed Abbas](https://www.linkedin.com/in/mohamed-abbas-k/)
- **Email**: [mohamedabbaskalandar@gmail.com](mailto:mohamedabbaskalandar@gmail.com)
