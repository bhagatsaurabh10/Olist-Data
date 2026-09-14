# Olist Brazilian E-Commerce Dataset

This repository contains the **Brazilian E-Commerce Public Dataset by Olist**, downloaded from Kaggle. The data is being used as a source for an end-to-end Azure data engineering project based on the **Medallion Lakehouse architecture**.

## Dataset Source

[Kaggle – Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

## Project Overview

The project demonstrates how raw e-commerce data can be ingested, transformed, enriched and served through a scalable Azure data platform.

The solution uses:

* Azure Data Factory
* Azure Data Lake Storage Gen2
* Azure Databricks
* PySpark
* Azure SQL Database
* MongoDB
* Azure Synapse Analytics

## Medallion Architecture

### Bronze Layer

Reusable, parameterised Azure Data Factory pipelines ingest source data from Azure SQL Database into the Bronze layer of ADLS Gen2 while preserving the original records.

### Silver Layer

Azure Databricks and PySpark are used to:

* Validate schemas
* Correct data types
* Handle missing values
* Remove duplicate records
* Standardise fields
* Join related e-commerce datasets
* Enrich the integrated data with MongoDB records
* Publish validated outputs to the Silver layer

### Gold Layer

The validated data is transformed into business-ready Gold datasets. Azure Synapse serverless SQL, external schemas, views and external tables make the curated information available for reporting and analytics.

## Dataset Files

| File                                    | Description                                         |
| --------------------------------------- | --------------------------------------------------- |
| `olist_customers_dataset.csv`           | Customer identifiers and location information       |
| `olist_geolocation_dataset.csv`         | Brazilian postcode coordinates and locations        |
| `olist_order_items_dataset.csv`         | Products, sellers, prices and freight values        |
| `olist_order_payments_dataset.csv`      | Payment methods, instalments and transaction values |
| `olist_order_reviews_dataset.csv`       | Customer review scores and comments                 |
| `olist_orders_dataset.csv`              | Order status and lifecycle timestamps               |
| `olist_products_dataset.csv`            | Product categories, dimensions and weight           |
| `olist_sellers_dataset.csv`             | Seller identifiers and locations                    |
| `product_category_name_translation.csv` | Portuguese-to-English product-category translations |

## Data Engineering Concepts Demonstrated

* End-to-end data pipeline development
* Medallion architecture
* Parameterised data ingestion
* Schema validation and data-quality checks
* PySpark transformations and joins
* Relational and NoSQL data integration
* Cloud data-lake organisation
* Serverless SQL querying
* Curated data serving for reporting and analytics

## Repository Purpose

This repository stores the source dataset used for educational data-engineering practice. The pipeline code and cloud resources may be maintained separately from the raw data repository.

## Acknowledgement

The dataset was published by Olist and obtained through Kaggle. Refer to the original Kaggle page for its documentation and usage conditions.
