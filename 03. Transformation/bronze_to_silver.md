### **Bronze to Silver Transformation**



The Bronze layer contains raw ingested data with minimal validation. The Silver layer represents cleaned and standardized data prepared for modeling.



Key transformations performed:



* Removed records with invalid or negative fare amounts and trip distances.
* Handled null values in critical columns such as timestamps and vendor identifiers.
* Standardized pickup and drop-off timestamp formats.
* Enforced consistent data types across numeric and datetime fields.
* Removed unnecessary raw ingestion metadata columns.



The Silver layer output is stored in a structured, file-based format. Delta tables were intentionally not created at this stage. This keeps the Silver layer lightweight and focused on data cleansing.



Implementation is available in `notebooks/bronze\_to\_silver.ipynb`.

