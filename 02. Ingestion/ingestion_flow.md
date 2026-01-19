### **Ingestion Flow**



* Data ingestion is implemented using Azure Data Factory (ADF).



* The pipeline iterates over all months of the year using a ForEach activity. Within the loop, an If Condition is used to handle differences in source file naming conventions between single-digit and double-digit months.



* Each branch of the condition triggers a parameterized Copy activity that dynamically constructs the source file path and ingests the data into the raw/bronze layer in cloud storage.



* This approach ensures reliable ingestion across all months while keeping the pipeline reusable and environment-agnostic.



