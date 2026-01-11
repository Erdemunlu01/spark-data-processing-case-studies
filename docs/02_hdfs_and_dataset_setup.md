# HDFS and Dataset Setup

This document describes how the datasets used in this project were **uploaded to HDFS** and how the directory structure was created.  
All steps are based on real commands executed in the terminal.

The purpose of this setup is to ensure that datasets are properly prepared on HDFS before starting Apache Spark processing.

---

## Datasets Used

Two main datasets are used in this project:

### 1. Dirty Store Transactions Dataset
- A retail transactions dataset containing dirty and inconsistent data
- Used in the Spark data cleaning case study

### 2. Retailer Dataset
- A multi-table CSV dataset used for business-oriented data analysis
- Includes the following tables:
  - categories
  - customers
  - departments
  - orders
  - order_items
  - products

---

## Downloading the Dataset (Local Environment)

The dataset was first downloaded to the local environment:

```bash
wget https://raw.githubusercontent.com/erkansirin78/datasets/refs/heads/master/dirty_store_transactions.csv
```

---

## Creating HDFS Directory Structure

Directories required for Spark processing were created on HDFS.

### For Dirty Store Transactions:

```bash
hdfs dfs -mkdir /user/train/datasets
hdfs dfs -mkdir /user/train/spark_odev_transaction
```

### For the Retailer Dataset:

```bash
hdfs dfs -mkdir /user/train/retailer_db
hdfs dfs -mkdir /user/train/retailer_db/categories
hdfs dfs -mkdir /user/train/retailer_db/customers
hdfs dfs -mkdir /user/train/retailer_db/departments
hdfs dfs -mkdir /user/train/retailer_db/orders
hdfs dfs -mkdir /user/train/retailer_db/order_items
hdfs dfs -mkdir /user/train/retailer_db/products
```

---

## Uploading Datasets to HDFS

### Dirty Store Transactions Dataset

```bash
hdfs dfs -put dirty_store_transactions.csv /user/train/datasets
```

This dataset is read by Spark during the data cleaning case study.

---

### Retailer Dataset CSV Files

```bash
hdfs dfs -put categories.csv /user/train/retailer_db/categories
hdfs dfs -put customers.csv /user/train/retailer_db/customers
hdfs dfs -put departments.csv /user/train/retailer_db/departments
hdfs dfs -put orders.csv /user/train/retailer_db/orders
hdfs dfs -put order_items.csv /user/train/retailer_db/order_items
hdfs dfs -put products.csv /user/train/retailer_db/products
```

This directory structure allows Spark to read each table separately from HDFS.

---

## Verifying the HDFS Structure

After uploading the datasets, the directory structure was verified using the following commands:

```bash
hdfs dfs -ls /user/train/datasets
hdfs dfs -ls /user/train/retailer_db
```

---

## Notes

- After being uploaded to HDFS, datasets are read directly from these directories by Spark
- The HDFS directory structure helps keep the case studies organized and easy to follow
- Only commands that were actually used in the project are included in this document

---

Once these setup steps are completed, the Spark notebooks are ready to be executed.
