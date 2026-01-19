### **Ingestion Layer**





This folder documents the ingestion layer implemented using Azure Data Factory. NYC Taxi trip data is ingested from the official NYC TLC public data source. Linked services are used to connect to the source and cloud storage securely. The pipeline iterates over monthly datasets using a ForEach activity. An If Condition is applied to handle differences in source file naming conventions. Parameterized datasets are used to dynamically construct source file paths. Data is ingested into the raw and bronze layers for downstream processing.



**Full pipeline exports and credentials are excluded due to environment-specific configurations.**

