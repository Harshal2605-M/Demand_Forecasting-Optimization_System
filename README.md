# Azure-Demand-Forecasting-Capacity-Optimization-System-Harshal-Mahajan

📊 Azure Demand Forecasting & Optimization
  End-to-End Cloud Architecture • Medallion Pipeline • Machine Learning • Power BI

Datasets : https://drive.google.com/drive/folders/1XvjtcjW7YeDTXliNYR1GO3NVVf91OdSx?usp=drive_link

Demo Video : https://drive.google.com/file/d/1u-Z3md5OW_4nuS0TExVk8N3y1axUG0Xs/view?usp=sharing

🚀 Project Overview

  This project showcases a complete end-to-end Demand Forecasting & Optimization system built using Azure Cloud, Databricks, and Power BI.

  It demonstrates how real enterprise data—coming from Snowflake, Amazon S3, and REST APIs—can be unified, processed, modeled, and visualized using a scalable architecture.

  Businesses can use this solution to:

  Analyze sales performance

  Forecast next-month demand per product

  Measure forecasting accuracy

  Understand customer behavior & conversion

  Optimize inventory & supply decisions

🗂️ Architecture Overview

  <img width="2524" height="912" alt="diagram-export-11-25-2025-11_33_13-AM" src="https://github.com/user-attachments/assets/7cd3f461-a15f-4931-8e1a-31a5debd3881" />


  The project integrates multiple technologies to simulate a real enterprise workflow:

  1.Data Sources

    Snowflake – Historical sales data

    Amazon S3 Bucket – Web behavior & log data

    REST API – Realtime product metadata

  2.Azure Components

    Azure Data Factory → Orchestrates ingestion pipelines

    Azure Data Lake Gen2 → Central data storage

    Azure Databricks → ETL + ML model training

  3.Medallion Architecture → Bronze, Silver, Gold layers

  4.Power BI → Final dashboard reporting

🧱 Medallion Architecture
  🔶 Bronze Layer – Raw Data

  i)Direct ingestion from Snowflake, S3, and API

  ii)Minimal transformations

  iii)Schema-aligned storage

  🔷 Silver Layer – Cleaned/Structured Data

  i)Handling missing values

  ii)Data standardization

  iii)Joining datasets (sales + logs + metadata)

  iv)Time-series feature creation (YearMonth, category mapping)

🟡 Gold Layer – Analytics & Modeling

  i)Aggregated datasets

  ii)Feature-engineered tables for ML

  iii)Clean tables for dashboards

🤖 Machine Learning Pipeline

  A dedicated Model Training Notebook trains forecasting models for every product individually.

  The workflow includes:

  i)Loop through each product

  ii)Train multiple models:

    ARIMA / SARIMA

    Moving Average (MA)

    Naïve Model

    Exponential Smoothing

    Prophet (optional)

  iii)Compute MAPE for all models

  iv)Select best model per product

  v)Generate next-month forecast

  vi)Store results in Gold tables

📊 Power BI Dashboards

  The final outputs are visualized through three interactive dashboards:

  1️⃣ Sales Overview Dashboard

  i)Total Sales, Avg Sales, Sales Quantity

  ii)Category-level contribution

  iii)YoY & MoM growth

  iv)Monthly Sales Trend

  v)Sales Target vs Actual

  <img width="1545" height="868" alt="Screenshot 2025-11-25 120004" src="https://github.com/user-attachments/assets/a03d029b-ee92-40b3-8bae-732cf1fba0a6" />


2️⃣ Forecasting Overview Dashboard

  i)Total Forecast Quantity

  ii)Average MAPE

  iii)Best Model per Product

  iv)MAPE Quality Distribution

  v)Forecast Reliability

  vi)Top 20 Products – Next Month Forecast

  vii)Forecast Confidence Gauge

  <img width="1548" height="877" alt="Screenshot 2025-11-25 120026" src="https://github.com/user-attachments/assets/ac0b6e7d-af5d-4e91-a995-fea9229ff6d2" />


3️⃣ Web Behavior & Conversion Dashboard

  i)Digital Demand Score

  ii)Views by Time of Day

  iii)Conversion Funnel (Visitors → Views → Add-to-Cart → Purchased)

  iv)Category-wise conversion patterns

  v)Linking customer behavior to demand

  <img width="1540" height="865" alt="Screenshot 2025-11-25 120110" src="https://github.com/user-attachments/assets/98a7f893-07a4-4e62-9105-340755a73bc2" />


🔧 Technologies Used

  i)Azure Data Factory

  ii)Azure Databricks (PySpark/Python)

  iii)Azure Data Lake Gen2

  iv)Snowflake

  v)Amazon S3

  vi)REST APIs

  vii)Power BI

  viii)ML models (ARIMA, MA, Naïve, ES, Prophet)

🎯 Key Outcomes

  i)Unified multi-source retail dataset

  ii)Automated ETL pipeline using Medallion architecture

  iii)Product-wise forecasting with model comparison

  iv)MAPE-based best model selection

  v)Production-ready dashboards for business decision-making



