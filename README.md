Failed Bank Transactions Analysis – GCP Data Pipeline

Project Overview

This project simulates a real-time banking scenario focusing on **failed transactions** across multiple branches in different cities. The objective is to build a complete data pipeline using Google Cloud Platform tools from **data generation** to **visual reporting**.

---

Data Generation

* Created **15 CSV files** representing failed bank transactions.
* The data covers:

  * **7 days**
  * **3 cities**
  * **5 branches per city**
* Each file simulates real-world banking failure scenarios inspired by insights from Deloitte banking articles.

---

Data Pipeline Workflow

1. **Upload to Cloud Storage (GCS):**

   * All 15 CSVs are uploaded to a GCS bucket.

2. **Data Filtering using PySpark:**

   * A PySpark script merges all CSVs.
   * Filters only rows with **failed transactions**.
   * Outputs a single **filtered CSV** back to GCS.

3. **Cloud SQL Integration:**

   * The filtered CSV file is connected to a Cloud SQL instance for structured access.

4. **BigQuery for Analysis:**

   * The Cloud SQL instance is linked to BigQuery.
   * Multiple SQL queries are executed for exploratory data analysis.

5. **Visualization via Looker Studio (Looker):**

   * Results are visualized using interactive dashboards and charts.

---

Tools Used

* **Google Cloud Storage (GCS)**
* **PySpark** (for merging and filtering)
* **Google Cloud SQL**
* **BigQuery**
* **Looker Studio** (for visualization)

---

Key Insights

* Identified most frequent error messages.
* Pinpointed top failing branches and cities.
* Found transaction types with highest failures.
* Time-based trends in failed transaction volumes.

---


