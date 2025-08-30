# olist-data-platform
End-to-end data engineering project on Azure Databricks using Olist E-commerce dataset (Medallion architecture: Bronze → Silver → Gold, with CI/CD, data quality, and optimization).

Problem Statement:
Olist is a Brazilian marketplace with rich transactional data: orders, customers, products, payments, reviews, and logistics. The challenge is to design and implement a production-grade data platform that ingests, cleans, models, and serves this data for analytics.

Scope & Approach:

Ingestion (Bronze): Load raw CSVs from Olist Kaggle dataset into ADLS Gen2 → Delta Bronze tables in Databricks.

Cleaning (Silver): Standardize data types, deduplicate customers, translate product categories, handle nulls, and enforce schema.

Modeling (Gold): Build a star schema with fact tables (orders, payments, reviews) and conformed dimensions (customer, product, seller, date).

Governance: Manage schema and permissions via Unity Catalog.

Orchestration: Use ADF / Databricks Jobs to automate pipelines.

Quality: Enforce data tests with Great Expectations / DLT expectations.

CI/CD: Use Databricks Asset Bundles for deployment across dev → prod.

Optimization: Apply Photon execution engine, partitioning, and Z-ORDER for performance.

Outcome:
A fully functioning end-to-end data engineering project demonstrating:

Medallion architecture (Bronze → Silver → Gold)

Data modeling skills (fact/dim design, SCD2, grain definition)

Data quality enforcement

Orchestrated + automated CI/CD pipelines

Production-ready best practices (cost/performance optimization)

Use Cases Enabled:

Sales analytics: revenue/margin by product, seller, customer segment

Delivery performance: actual vs estimated SLA

Customer feedback: review trends, satisfaction metrics

Payments analysis: payment types, value distribution, installments
