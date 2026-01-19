### **Silver to Gold Transformation**



The Silver layer provides clean and standardized data suitable for modeling. The Gold layer is designed for analytics, reporting, and BI consumption.



Key modeling decisions:



* Created an analytics-ready fact table representing taxi trips.
* Derived supporting dimension-style attributes for vendor, time, and location analysis.
* Applied business-friendly column naming and metric derivations.
* Optimized data structure for aggregation and reporting workloads.



Delta tables are created in the Gold layer to support ACID guarantees and performance. Due to restricted admin access, Delta tables were not registered using saveAsTable. Instead, Delta tables were created within an existing database using an alternative approach, ensuring compatibility with the environment while preserving design intent.



Implementation is available in `notebooks/silver\_to\_gold.ipynb`.

