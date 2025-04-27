#Shipping Data Pipeline

An end-to-end data engineering pipeline that processes near real-time shipping events using Spark, and loads the data into BigQuery. Managed using Airflow.

## Stack:
- Python 3.12.2
- Apache Spark 3.5.5
- Apache Airflow 2.x (edit)
- Google BigQuery

## Folder Structure:
- 'airflow_dags/' → Airflow DAG definitions
- 'acquisition/' → Scripts to acquire shipping events
- 'processing/' → Spark ETL scripts
- 'bigquery/' → BigQuery DDLs and queries
- 'config/' → Configurations (like GCP credentials)
- 'utils/' → Utility functions
- 'tests/' → Unit tests
- 'data/' → Sample raw and processed data
- 'notebooks/' → Jupyter exploration notebooks

## Setup: (edit)
1. Install dependencies:

   pip install -r requirements.txt
   

2. Configure `config/config.yaml`:
   ```
   gcp_project_id: "your-gcp-project"
   bq_dataset: "your_dataset"
   gcs_bucket: "your_bucket"
   ```

3. Run Airflow Scheduler:
   ```
   airflow scheduler
   airflow webserver
   ```

4. Trigger the DAG `shipping_etl_dag` to run the pipeline.

## Author:
- Yaswanth Kandregula
- www.linkedin.com/in/yaswanth-kandregula-7b110762

