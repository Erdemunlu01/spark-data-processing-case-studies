# Case Study — Real Data Processing and Business-Oriented Analysis

This document consolidates the work performed in the  
`spark_retailer_dataset_annotated` notebooks  
into a **single, unified case study**.

The documentation is prepared by strictly following the **existing code** in both notebooks.  
No code modifications or additions have been made.

The purpose of this case study is to demonstrate, in one continuous flow, how Apache Spark is used to:
- Read real-world datasets from HDFS
- Process data using the Spark DataFrame API
- Perform business-oriented analysis on multiple related tables

---

## Case Study Overview

In this study, real retailer datasets are used.  
All data is stored on HDFS and processed using Apache Spark.

The case study consists of two main stages:
1. Processing real-world data with Spark  
2. Performing multi-table, business-oriented analysis

This structure represents an **end-to-end data processing scenario** commonly encountered in real-world projects.

---

## Datasets Used

The following CSV tables are used in this study:

- categories  
- customers  
- departments  
- orders  
- order_items  
- products  

These tables represent operational data of a retailer and are logically related to each other.

---

## Reading Data from HDFS

As the first step, all datasets are read from their respective HDFS directories into Spark DataFrames.

At this stage:
- Each table is read separately from HDFS paths
- CSV format is used
- Spark DataFrame abstraction is applied

This approach provides a scalable and distributed data processing foundation.

---

## Real Data Processing with Spark

After loading the datasets into Spark DataFrames:
- Required columns are selected
- Basic filtering operations are applied
- Data is prepared in a structure suitable for analysis

The goal of this step is to gain hands-on experience processing real data using the Spark DataFrame API.

---

## Multi-Table Analysis and Join Operations

To address business requirements:
- Relationships between multiple tables are established
- Join operations are performed using common keys
- Necessary data combinations are created for analysis

This step demonstrates how Spark can be used for **relational-style analysis** on distributed datasets.

---

## Business-Oriented Analysis

The analyses performed in this study are:
- Designed to support business scenarios
- Implemented using the Spark DataFrame API
- Intended to produce outputs that can be used for decision support

The focus is on generating **meaningful and actionable data outputs**, rather than technical complexity.

---

## Analysis Outputs

As a result of all processing steps:
- Analysis-ready result DataFrames are produced
- These outputs can be reused for reporting or further analytical tasks

This confirms that the real data processing and business analysis workflow has been successfully completed using Spark.

---

## Notes

- The code inside the notebooks is **not modified**
- This document focuses on explaining what is done and why it is done
- The case study is designed to closely reflect real-world Spark data processing scenarios

---

This case study provides a comprehensive example of using Apache Spark  
to process real datasets and perform business-oriented analysis in an end-to-end manner.
