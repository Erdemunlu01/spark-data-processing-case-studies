# Case Study 1 — Data Cleaning with Apache Spark

This document explains the **data cleaning steps** performed in the `spark_data_cleaning.ipynb` notebook.  
All steps described here strictly follow the **existing code** in the notebook, without any modifications.

The goal of this case study is to demonstrate how a dirty CSV dataset can be made **analysis-ready** using Apache Spark.

---

## Case Study Overview

The dataset used in this case study is a retail transactions CSV file that contains **dirty and inconsistent data**.

The main issues observed in the dataset include:
- Inconsistent text values in certain fields (`STORE_LOCATION`)
- Price columns stored as strings with a `$` symbol
- Numeric fields not suitable for direct analysis

These issues are addressed step by step using the Spark DataFrame API.

---

## Reading the Data with Spark

As a first step, the dataset is read from HDFS into a Spark DataFrame.

At this stage:
- The data is read in CSV format
- The header option is enabled
- All columns are initially read as strings

This approach makes it easier to control type casting and transformations during the data cleaning process.

---

## Cleaning the STORE_LOCATION Field

The `STORE_LOCATION` field contains inconsistent values such as:
- `New York(`
- `New York+`
- `New York `

In this step:
- Unwanted characters are removed
- Extra whitespace is eliminated
- Location values are normalized into a single standard format

As a result, location-based analyses become more reliable and consistent.

---

## Cleaning Price Columns

The following price-related columns contain the `$` symbol:
- `MRP`
- `CP`
- `DISCOUNT`
- `SP`

In this step:
- The `$` character is removed from string values
- Columns are cast to appropriate numeric data types

This allows mathematical operations to be performed on price values.

---

## Data Type Conversions

As part of the data cleaning process:
- Numeric columns are cast to suitable numeric types
- Date fields are converted into analysis-friendly formats

These steps provide a clean foundation for further analysis in Spark.

---

## Final Clean Dataset

After completing all data cleaning steps:
- Dirty and inconsistent values are removed
- A clean Spark DataFrame suitable for analysis is obtained

This cleaned dataset can be reused in later analyses or additional case studies.

---

## Notes

- The code inside the notebook is **not modified**
- This document focuses on explaining what each step does and why it is performed
- All transformations are implemented using the Spark DataFrame API

---

This case study provides a practical example of basic data cleaning using Apache Spark.
