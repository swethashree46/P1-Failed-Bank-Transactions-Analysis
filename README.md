# Failed Banking Transaction Analysis
Project Overview
This project builds a scalable data pipeline to ingest, clean, analyze, and store banking transaction data from multiple branches. The focus is on identifying and analyzing failed transactions across different cities for operational insights and strategic decision-making.

---

Data Sources
- **CSV Files**: Daily transaction data from 15 branches (5 per city) over a 7-day period.
- **Storage**: Uploaded to Google Cloud Storage using `gsutil`.

---

Technologies Used
- **Google Cloud Storage (GCS)** – Raw data storage
- **Google Cloud Dataproc** – PySpark job execution
- **PySpark** – Data cleaning, aggregation, and transformation
- **Cloud SQL (MySQL)** – Storage of failed transaction records
- **BigQuery** – SQL-based data analysis and visualization

---

Pipeline Steps

1. **Data Ingestion**
   - Upload CSV files to a GCS bucket using `gsutil`.
   - Maintain structured folder hierarchy for city/branch data.

2. **Data Cleaning & Aggregation**
   - Run PySpark job on Dataproc to:
     - Load multiple CSV files.
     - Remove null or blank rows.
     - Merge into a single clean CSV file.

3. **Filtering Failed Transactions**
   - Run a second PySpark job to:
     - Identify failed transactions based on status codes or keywords.
     - Save results to Cloud SQL (MySQL) for persistent storage.

4. **Data Analysis**
   - Use BigQuery to:
     - Query failed transaction patterns.
     - Analyze impact by branch, city, and time window.
     - Prepare data for dashboards and reporting.

---

Key Outcomes
- Centralized and cleaned transactional data from 15 branches.
- Automated identification of failed transactions.
- Seamless integration with BigQuery for analytics and insights.

---

Example Use Cases
- Track failure rates per branch or city.
- Identify common failure reasons (e.g., network errors, timeouts).
- Measure impact on customer experience and system reliability.

---

Future Improvements
- Automate pipeline with Cloud Composer (Airflow).
- Add alerting for high failure rates.
- Integrate real-time streaming via Pub/Sub and Dataflow.

---



