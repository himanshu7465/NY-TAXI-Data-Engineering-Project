# NYC Taxi End-to-End Data Engineering Project

## Project Overview
This project demonstrates a **complete end-to-end data engineering pipeline** for NYC Taxi trip data using **Azure cloud services, Databricks, and Power BI**, following the **medallion architecture** (Bronze → Silver → Gold).  

The pipeline ingests raw trip data from the NYC Taxi API, transforms and cleans it, and delivers curated datasets for analytics and visualization. The project emphasizes **scalability, reliability, and maintainability**, incorporating **Delta Lake features** like versioning and time travel.

<img width="754" height="614" alt="Screenshot 2025-08-17 at 20 25 14" src="https://github.com/user-attachments/assets/0a961518-ea1c-4345-a2c1-6fd796d26d2a" />
---

## Project Objectives
- Efficiently ingest raw NYC Taxi data into a cloud data lake.
- Implement **cleaning and transformation logic** for analytical-ready data.
- Organize data using **medallion architecture** for reliability and performance.
- Enable **versioning and historical tracking** using Delta Lake.
- Provide **interactive dashboards** and insights in Power BI.
- Demonstrate **cloud-native data engineering best practices**.

---

## Architecture & Workflow

### 1️⃣ Data Ingestion (Bronze Layer)
- **Source:** NYC Taxi API (Trip Data) Link : https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page  
- **Tool:** Azure Data Factory (ADF)  
- **Process:**
  - ADF pipelines fetch data from the API periodically.
  - Raw data is stored in **Azure Data Lake Storage Gen2** in the Bronze layer.
- **Data format:** Raw JSON/CSV  
- **Purpose:** Maintain raw, unprocessed data as the source of truth.

  <img width="2402" height="1756" alt="image" src="https://github.com/user-attachments/assets/d2c4f7bf-19cd-400f-afff-ef69b0b7c6ee" />
  <img width="2398" height="1752" alt="image" src="https://github.com/user-attachments/assets/4555629d-e02a-4b1e-8252-9ae692af5368" />
  <img width="2400" height="1730" alt="image" src="https://github.com/user-attachments/assets/ba2133d0-e744-4f0b-880a-e483ee94c63e" />





---

### 2️⃣ Data Transformation (Silver Layer)
- **Tool:** Azure Databricks (Apache Spark)  
- **Process:**
  - Transform raw data into a **cleaned and structured format**.
  - Handle missing values, data type corrections, and normalization.
  - Store processed data in **Parquet format** for intermediate analytics.
- **Layer Name:** Silver  
- **Purpose:** Prepare data for analytics while maintaining high performance and storage efficiency.

<img width="2400" height="1754" alt="image" src="https://github.com/user-attachments/assets/145aac73-2497-4149-a7ca-906798c4e9da" />
<img width="2404" height="1746" alt="image" src="https://github.com/user-attachments/assets/2776cea5-fb89-4491-88c7-1ecf63c1270a" />
<img width="2400" height="1748" alt="image" src="https://github.com/user-attachments/assets/0acbb54a-ed1f-46ce-8217-bf9b5c27e827" />
<img width="2400" height="1748" alt="image" src="https://github.com/user-attachments/assets/a0eb88c6-bfe0-4e17-8d60-6cbe945799f0" />



---

### 3️⃣ Data Modeling & Curation (Gold Layer)
- **Tool:** Delta Lake in Databricks  
- **Process:**
  - Curate analytical-ready datasets with **business-level metrics**.
  - Convert cleaned Parquet data into **Delta Tables**.
  - Implement **versioning and time travel** for data auditability and rollback.
- **Layer Name:** Gold  
- **Purpose:** Create **reliable, production-ready datasets** for reporting and analytics.
  <img width="2402" height="1752" alt="image" src="https://github.com/user-attachments/assets/17d6c017-5dde-4cf7-8fcc-0daaf8f064f2" />
<img width="2402" height="1760" alt="image" src="https://github.com/user-attachments/assets/0ef2a5de-4b8c-44da-a96d-1343397f418b" />
<img width="2398" height="1754" alt="image" src="https://github.com/user-attachments/assets/d20146fa-0d77-4f37-bbc0-9fcd03341ced" />
<img width="2402" height="1756" alt="image" src="https://github.com/user-attachments/assets/c0e23a12-6cb2-4186-b948-307b043bd789" />




---

### 4️⃣ Data Visualization
- **Tool:** Power BI  
- **Process:**
  - Connect Azure Databricks to Power BI using an **access token**.
  - Build **dashboards** to analyze trip counts, fares, peak hours, and geographic patterns.
  - Use curated Gold layer data for accurate and fast reporting.

<img width="2400" height="1752" alt="image" src="https://github.com/user-attachments/assets/ec99def2-e67f-4e3b-8278-a45e691595fc" />
  <img width="1440" height="900" alt="Screenshot 2025-08-17 at 19 11 32" src="https://github.com/user-attachments/assets/9d5d40cb-8760-4c5b-a117-20467e87847a" />
<img width="1440" height="900" alt="Screenshot 2025-08-17 at 19 13 04" src="https://github.com/user-attachments/assets/eb990340-fac4-413d-bb7b-d85515daea07" />


---

## Key Features
- **End-to-End Pipeline:** From API ingestion to visualization.  
- **Medallion Architecture:** Bronze (raw) → Silver (transformed) → Gold (curated).  
- **Cloud-Native Implementation:** Fully on Azure Data Platform.  
- **Delta Lake Features:** Versioning & time travel for historical tracking.  
- **Data Transformation:** Cleaning, normalization, type casting, and Parquet storage.  
- **Power BI Integration:** Real-time dashboards using access tokens.  
- **Scalability:** Designed to handle large-scale NYC Taxi datasets.

---

## Technologies Used
- **Azure Data Factory** – Pipeline orchestration & ingestion  
- **Azure Databricks** – Spark-based transformations & Delta Lake  
- **Delta Lake** – Versioned tables, time travel, ACID compliance  
- **Parquet Format** – Efficient intermediate storage  
- **Power BI** – Data visualization and reporting  
- **Medallion Architecture** – Layered approach for scalable data engineering  

---

## Learning Outcomes / Skills Demonstrated
- Building **cloud-based ETL pipelines** with Azure Data Factory  
- Designing and implementing **medallion architecture**  
- Using **Apache Spark for data transformation** at scale  
- Working with **Delta Lake features** such as versioning and time travel  
- Connecting Databricks to **Power BI** for business analytics  
- Applying **best practices in data engineering** for reliability and maintainability


