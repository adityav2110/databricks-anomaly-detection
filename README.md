# databricks-anomaly-detection

📘 Databricks Anomaly Detection Pipeline (End-to-End)

This project demonstrates a complete anomaly detection solution designed for enterprise data engineering and AI teams.

It includes:

✔ 1. Data Ingestion

Sales and Inventory tables are loaded into Databricks (simulated using CSV files).
In real deployment, these would come from Data Lake or Snowflake.


---

✔ 2. Technical Data Quality (TDQ)

The pipeline checks:

Null values

Duplicate records

Schema validation

Record count stability


A TDQ summary table is generated for reporting.


---

✔ 3. Business Data Quality (BDQ)

Rules applied based on expected business logic:

Sales amount must be positive

Dates cannot be in the future

Inventory stock cannot be negative


Violations are flagged in a BDQ table.


---

✔ 4. ML-Based Time Series Anomaly Detection

An Isolation Forest model is used to find unusual transactions:

Unusual amount spikes

Abnormal quantity values

Out-of-pattern events


Each record receives:

an anomaly score

an anomaly label



---

✔ 5. Predictive Rules

On top of ML anomalies, domain rules are added:

High-value transaction (> 50,000)

Suspicious discounts

ML-detected anomalies


A final risk flag is assigned.


---

✔ 6. Final Output

The pipeline produces a consolidated Delta Table containing:

TDQ issues

BDQ violations

ML anomaly detection

Predictive rule flags

Overall risk score


This table is ready for dashboards, alerting pipelines, and monitoring.


---

🚀 Technologies Used

PySpark / Databricks

Isolation Forest (ML)

Delta Lake

Python

Pandas



---

📎 Notebook

notebooks/anomaly_detection_databricks.ipynb


---

📁 Data Inputs

sales.csv

inventory.csv



---

🏁 Status

Ready for review and evaluation.
