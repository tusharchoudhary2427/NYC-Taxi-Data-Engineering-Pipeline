### **Parameterization Logic**



During ingestion, the source files followed different naming patterns for single-digit and double-digit months.

This caused ingestion failures when processing months beyond September using a static file path approach.



To resolve this, dataset-level parameterization was introduced to dynamically construct source paths based on runtime values.

The pipeline evaluates the month value and applies conditional logic to determine the correct file naming format.



Parameterized datasets are used within Copy activities to avoid hardcoded paths and improve reusability.

This design allows the same pipeline to ingest data across all months without manual intervention.



The approach improves scalability, reduces duplication, and aligns with production-style ingestion practices.

