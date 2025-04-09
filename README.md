# 📊 Data Pipeline with Airflow & AWS: ENEM PDF Processing

This project showcases a **data pipeline using Apache Airflow and AWS services** (S3, Lambda, and Glue) to automate the download, processing, and transformation of **ENEM exam PDFs** into structured data.

The pipeline is containerized using **Docker Compose**, and each component of the architecture—Airflow DAGs, AWS Lambda functions, and Glue jobs—is included for a fully reproducible, end-to-end ETL workflow.

---

## 🚀 Pipeline Overview

1. **Download ENEM PDFs**: `download_files.py` downloads PDFs from a public source.
2. **Upload to S3**: Airflow DAG or script uploads them to a raw S3 bucket.
3. **Trigger Lambda**: An S3 event triggers `lambda_function.py`, which invokes a Glue job.
4. **Transform with Glue**: `process_pdf_glue_job.py` processes and parses data from PDFs, storing the transformed output in another S3 bucket.
5. **Airflow DAG**: `process_enem_pdf.py` orchestrates this end-to-end pipeline.

---

## 📌 Medium Article Reference

Original concept from the blog post:  
👉 [**Data Pipeline with Airflow and AWS Tools (S3, Lambda, Glue)**](https://medium.com/data-science/data-pipeline-with-airflow-and-aws-tools-s3-lambda-glue-18585d269761)

---

## ✅ Features

- 📥 Automated PDF download  
- ☁️ AWS S3 integration  
- 🔁 Serverless Lambda trigger  
- 🔄 Glue-based ETL job  
- ⏱️ Orchestration with Apache Airflow  
- 🐳 Dockerized setup for local testing  

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
