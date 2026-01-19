### **Transformation Layer**



This folder documents the transformation logic applied to the NYC Taxi dataset. Transformations are organized into Bronze-to-Silver and Silver-to-Gold stages. The focus is on data quality, schema standardization, and analytics readiness.



The Silver layer contains cleaned and standardized data stored in file-based format. The Gold layer contains analytics-ready Delta tables used for reporting and analysis.



Due to restricted admin access, Delta tables were not created using saveAsTable. Instead, Delta tables were created in the Gold layer using a database-compatible approach.





