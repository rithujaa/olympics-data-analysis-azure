# Tokyo Olympics Data Engineering Pipeline — Azure Data Factory, Databricks & Synapse

This project demonstrates an **end-to-end Azure Data Engineering pipeline** for the **Tokyo Olympics dataset**, showcasing how raw data can be ingested, transformed, and analyzed using modern cloud technologies.  
The pipeline integrates multiple Azure services such as **Data Factory**, **Data Lake Storage Gen2**, **Databricks**, and **Synapse Analytics** to build a scalable, automated ETL framework.

![Project Architecture](./Data%20source.png)

---

## Architecture

| Stage | Service | Description |
|--------|----------|-------------|
| **Data Source** | GitHub (CSV Datasets) | Publicly available Tokyo Olympics datasets (Athletes, Coaches, EntriesGender, Medals, Teams) |
| **Data Integration** | Azure Data Factory | Ingests raw CSV files from GitHub into Azure Data Lake Storage Gen2 (Raw zone) |
| **Raw Data Store** | Azure Data Lake Gen2 | Stores unprocessed raw data for traceability and reprocessing |
| **Transformation** | Azure Databricks (PySpark) | Cleans, casts data types, performs transformations and aggregations |
| **Transformed Data Store** | Azure Data Lake Gen2 | Stores the transformed, analytics-ready data |
| **Analytics** | Azure Synapse Analytics | Enables SQL-based querying and visualization of the transformed data |

---

## Datasets Used
| Dataset | Description |
|----------|-------------|
| **Athletes.csv** | Contains athlete details participating in the Olympics |
| **Coaches.csv** | Lists coaches and associated teams |
| **EntriesGender.csv** | Tracks number of male, female, and total participants per discipline |
| **Medals.csv** | Medal tally by country/team |
| **Teams.csv** | Team-level data including countries and disciplines |

---

## Technologies & Tools
- **Azure Data Factory** – Data ingestion from GitHub to ADLS Gen2  
- **Azure Data Lake Storage Gen2** – Raw and transformed data zones  
- **Azure Databricks** – PySpark-based data cleaning, transformation, and analysis  
- **Azure Synapse Analytics** – SQL-based data exploration and reporting  
- **Python (PySpark)** – Transformation and analysis logic  

---

## Key Transformations (PySpark)
- Mounted Azure Data Lake Storage Gen2 using **OAuth credentials**
- Loaded multiple CSVs (`athletes`, `coaches`, `entriesgender`, `medals`, `teams`) from raw zone
- Casted columns (e.g., Female, Male, Total) into appropriate numeric types
- Calculated:
  - Top-performing countries by **Gold medals**
  - Average gender participation ratios per discipline
- Wrote transformed data back to **ADLS Gen2 (transformed zone)** for downstream analysis

---

## Learning Outcomes
- Building **ETL pipelines** using Azure Data Factory, Databricks, and Synapse
- Working with **Azure Data Lake Gen2** and **OAuth authentication**
- Performing transformations and aggregations using **PySpark**
- Designing a **modular, scalable data architecture** for analytics workloads

---
## Contact
If you’re also exploring data engineering or cloud projects — I’d love to connect!
  
