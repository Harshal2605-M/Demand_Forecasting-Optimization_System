# Azure-Demand-Forecasting-Capacity-Optimization-System-Harshal-Mahajan

This is project file of Azure based Demand Forecasting and Capacity Optimization System of Infosys Springboard 6.0 Internship

📊 Azure Demand Forecasting & Optimization
End-to-End Cloud Architecture • Medallion Pipeline • Machine Learning • Power BI


🚀 Project Overview

This project showcases a complete end-to-end Demand Forecasting & Optimization system built using Azure Cloud, Databricks, and Power BI.
It demonstrates how real enterprise data—coming from Snowflake, Amazon S3, and REST APIs—can be unified, processed, modeled, and visualized using a scalable architecture.
Businesses can use this solution to:


  1.Analyze sales performance
  
  2.Forecast next-month demand per product
  
  3.Measure forecasting accuracy
  
  4.Understand customer behavior & conversion
  
  5.Optimizes inventory & supply decisions
  
Architecture of the project:-

<img width="2524" height="912" alt="diagram-export-11-25-2025-11_33_13-AM" src="https://github.com/user-attachments/assets/81a3a768-50a2-440a-acc6-aa92b55d25d9" />


🗂️ Architecture Overview

The project integrates multiple technologies to simulate a real enterprise workflow:

  1)Data Sources
  
  i)Snowflake – Historical sales data
  
  ii)Amazon S3 Bucket – Web behavior & log data
  
  iii)REST API – Realtime product metadata

  2)Azure Components
  i)Azure Data Factory → Orchestrates ingestion pipelines
  
  ii)Azure Data Lake Gen2 → Central data storage
  
  iii)Azure Databricks → ETL + ML model training
  
  iv)Medallion Architecture → Bronze, Silver, Gold layers
  
  v)Power BI → Final dashboard reporting


🧱 Medallion Architecture 

  🔶 Bronze Layer – Raw Data
  
  Direct ingestion from Snowflake, S3, and API
  
  Minimal transformations
  
  Schema-aligned storage



  🔷 Silver Layer – Cleaned/Structured Data
  Handling missing values
  
  Data standardization
  
  Joining datasets (sales + logs + metadata)
  
  Time-series feature creation (YearMonth, category mapping)



  🟡 Gold Layer – Analytics & Modeling
  
  Aggregated datasets
  
  Feature-engineered tables for ML
  
  Clean tables for dashboards



🤖 Machine Learning Pipeline

A dedicated Model Training Notebook trains forecasting models for every product individually.

The workflow includes:
  1.Loop through each product
  
  2.Train multiple models:
  
    i)ARIMA / SARIMA
    
    ii)Moving Average (MA)
    
    iii)Naïve Model
    
    iv)Exponential Smoothing
    
    v)Prophet 
    
  3.Compute MAPE for all models
  
  4.Select best model per product
  
  5.Generate next-month forecast
  
  6.Store results in Gold tables



📊 Power BI Dashboards

The final outputs are visualized through three interactive dashboards:

1️⃣ Sales Overview Dashboard

Total Sales, Avg Sales, Sales Quantity

Category-level contribution

YoY & MoM growth

Monthly Sales Trend

Sales Target vs Actual

<img width="1687" height="960" alt="image" src="https://github.com/user-attachments/assets/7f46ec8c-abec-4b36-b2fc-1cbd01503de6" />


2️⃣ Forecasting Overview Dashboard

Total Forecast Quantity

Average MAPE

Best Model per Product

MAPE Quality Distribution

Forecast Reliability

Top 20 Products – Next Month Forecast

Forecast Confidence Gauge

<img width="1707" height="960" alt="image" src="https://github.com/user-attachments/assets/ff65e8ae-29d1-4944-b74c-8ee228da47f1" />


3️⃣ Web Behavior & Conversion Dashboard

Digital Demand Score

Views by Time of Day

Conversion Funnel (Visitors → Views → Add-to-Cart → Purchased)

Category-wise conversion patterns

Linking customer behavior to demand

<img width="1677" height="949" alt="image" src="https://github.com/user-attachments/assets/b6b3304d-c424-4264-9750-9651cf8dd2f5" />


🔧 Technologies Used
  Azure Data Factory
  
  Azure Databricks (PySpark/Python)
  
  Azure Data Lake Gen2
  
  Snowflake
  
  Amazon S3
  
  REST APIs
  
  Power BI
  
  ML models (ARIMA, MA, Naïve, ES, Prophet)



🎯 Key Outcomes

  Unified multi-source retail dataset
  
  Automated ETL pipeline using Medallion architecture
  
  Product-wise forecasting with model comparison
  
  MAPE-based best model selection
  
  Production-ready dashboards for business decision-making
