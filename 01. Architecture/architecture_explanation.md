### **Project Overview**



This project implements a cloud-native data engineering pipeline on Azure to ingest, transform, and serve NYC Taxi trip data using a Lakehouse architecture.



### **Architecture Summary**



Data is ingested from source systems via Azure Data Factory and stored in Azure Data Lake Gen2. Transformations are handled in Databricks using PySpark, following Medallian architecture approach. Final datasets are stored as Delta tables for analytics and reporting.



### **Data Flow**



1. **Ingestion (ADF):** 

   	Source data is ingested monthly using a ForEach loop.
   	An If Condition handles single-digit vs double-digit month file naming.
   	Parameterized Copy activities load data into the Bronze layer.
   
1. 
**2. Bronze Layer (Raw):**

	Raw data stored in Parquet format in ADLS Gen2.
	No transformations applied.


**3. Silver Layer (Transformed):**
	
	Data cleaned, structured, and standardized using PySpark in Databricks.
	Stored as Parquet in ADLS Gen2.


**4. Gold Layer (Serving):**

	Curated datasets written as Delta tables.
	Ready for BI tools and analytics workloads.









