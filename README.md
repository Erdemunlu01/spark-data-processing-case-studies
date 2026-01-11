# Spark Data Processing Case Studies

This repository contains **three practical Apache Spark case studies** based entirely on hands-on work.  
The studies focus on **data cleaning**, **real-world data processing**, and **business-oriented data analysis** using CSV datasets stored on **HDFS**.

The purpose of this repository is to demonstrate a clear and simple Spark workflow without unnecessary complexity:
- Dataset setup on HDFS
- Data processing with Spark
- Producing analysis-ready outputs

All documentation explains **what is done** and **why it is done**, without modifying the original code.

---

## Case Studies

### Case Study 1 — Data Cleaning with Apache Spark

In this case study, a dirty retail transactions dataset is cleaned using Apache Spark.

The following steps are performed:
- Normalizing inconsistent `STORE_LOCATION` values  
  (e.g. `New York(`, `New York+`, `New York ` → `New York`)
- Removing the `$` symbol from price-related columns  
  (`MRP`, `CP`, `DISCOUNT`, `SP`)
- Casting string values to numeric data types
- Creating a clean dataset ready for further analysis

Notebook:
- `notebooks/spark_data_cleaning.ipynb`

Documentation:
- `docs/03_case1_data_cleaning.md`

---

### Case Study 2 — Real Data Processing

This case study focuses on processing a real-world dataset using Apache Spark.  
The goal is to practice core Spark DataFrame operations on real data stored on HDFS.

This study includes:
- Reading a real dataset from HDFS
- Applying Spark DataFrame transformations
- Filtering and transforming data
- Producing outputs suitable for analysis

Notebook:
- `notebooks/spark_retail_data_processing.ipynb`

Documentation:
- `docs/04_case2_real_data_processing.md`

---

### Case Study 3 — Business-Oriented Data Analysis

In this case study, multiple retailer-related CSV tables are analyzed based on business needs using Apache Spark.

The dataset includes:
- categories
- customers
- departments
- orders
- order_items
- products

The analysis focuses on:
- Reading multiple datasets from HDFS
- Applying joins and transformations aligned with business questions
- Producing analysis-oriented datasets

Notebook:
- `notebooks/spark_business_data_analysis.ipynb`

Documentation:
- `docs/05_case3_business_data_analysis.md`

---

## How to Use

1. Review the documentation files under the `docs/` directory to understand the project structure.
2. Set up the datasets on HDFS by following:
   - `docs/02_hdfs_and_dataset_setup.md`
3. Open and run the notebooks in the `notebooks/` directory using Jupyter Notebook or a Spark-supported environment.
4. Execute the notebooks based on the case study you want to explore.

---

## Requirements

- Apache Spark (PySpark)
- HDFS (Hadoop)
- Jupyter Notebook environment
- Postgresql

---

## Notes

- The code inside the notebooks is kept unchanged.
- Documentation focuses on explaining what each step does and why it is required.
- This repository emphasizes practical Spark usage rather than advanced theory.

---

## Author

Erdem Ünlü
