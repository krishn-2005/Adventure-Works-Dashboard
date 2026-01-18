🚲 AdventureWorks: End-to-End Business Intelligence Solution
!(https://img.shields.io/badge/Power_BI-Desktop-yellow?style=flat&logo=powerbi) !(https://img.shields.io/badge/DAX-Advanced-green) !(https://img.shields.io/badge/Data_Modeling-Snowflake_Schema-orange)

📖 Project Overview
This project is an advanced end-to-end Business Intelligence solution designed for AdventureWorks, a global manufacturing company. The goal was to transform raw sales, returns, and customer data into an interactive, actionable dashboard for executive decision-making.

The solution tracks KPIs (Revenue, Profit, Returns), analyzes regional performance, and identifies high-value customer segments using advanced DAX, data modeling, and dynamic user experiences.

💼 Business Problem
The management team required a way to track sales performance and profitability across global territories. Key requirements included:

Tracking KPIs: Monitor Revenue, Profit, and Total Orders against targets.

Product Intelligence: Identify high-return products and simulate pricing scenarios.

Customer Insights: Segment customers by income and occupation to reduce churn.

Regional Analysis: Visualize performance across North America, Europe, and the Pacific.

🛠️ Technical Architecture
1. Data Transformation (ETL)
Source: Raw CSV files (Sales, Returns, Customers, Products, Territories).

Transformation: Used Power Query (M) to build an automated folder-based ingestion pipeline.

Cleaning: performed data type validation, conditional column creation (e.g., Customer Income Groups), and text parsing for SKU segmentation.

2. Data Modeling
Schema Design: Designed a Snowflake Schema to handle complex product hierarchies (Category -> Subcategory -> Product).

Multi-Fact Model: Integrated distinct fact tables (Sales Data and Returns Data) using shared dimension tables.

Date Intelligence: Created a dynamic Rolling Calendar table using M-code to ensure contiguous date ranges for time-series analysis.

Role-Playing Dimensions: Utilized inactive relationships and USERELATIONSHIP to analyze data by both Order Date and Stock Date.

3. Advanced DAX Calculations
Engineered 40+ measures using complex DAX patterns:

Time Intelligence: 10-day Rolling Revenue, MoM Growth %, YTD Profit.

Parametrization: Created dynamic "What-If" parameters to simulate Price Adjustments and forecast their impact on Total Profit.

Context Manipulation: Used CALCULATE, ALL, and KEEPFILTERS for "Part-to-Whole" analysis (e.g., % of All Returns).

Iterator Functions: Implemented SUMX for row-level profitability calculations across related tables.

📊 Dashboard Features
The report consists of 4 interactive pages:

1. Executive Summary
A high-level view for C-Suite stakeholders.

Key Features: KPI Cards with trend indicators, Revenue Trending Line Chart, and Top 10 Product tables.

Insight: "Water Bottle - 30 oz." is the highest volume product, while specific regions show varying return rates.

2. Map Analysis
Geospatial intelligence visualization.

Key Features: Bing Maps integration showing Orders by City/State.

Insight: Visualized high-return clusters in European territories to flag logistics issues.

3. Product Detail
A deep dive into product performance.

Key Features:

Field Parameters: Allows users to dynamically toggle charts between Revenue, Orders, and Profit.

Price Adjustment Slider: A predictive tool allowing users to see how a 10% price increase would impact total profit.

Gauge Charts: Visualizing monthly performance against targets.

4. Customer Detail
Demographic and behavioral analysis.

Key Features:

Decomposition Tree: AI-driven root cause analysis for customer churn and revenue drivers.

Demographic Slicers: Analysis by Income Level and Occupation (Skilled Manual, Professional, etc.).

Top 100 Customers: A ranked list of high-value clients for loyalty targeting.

🚀 Key Insights & Business Value
Revenue Growth: Tracked $24.9M in total revenue with a steady upward trend in 2022.

Return Rate Optimization: Identified a 2.2% overall return rate, with specific "High Return" outliers flagged for QA review.

Customer Segmentation: Discovered that "Professional" and "Management" occupation sectors drive the highest average revenue per customer ($1,431).

Scenario Planning: The "What-If" analysis revealed that a 5% price increase on "Bikes" could yield significant profit margin improvements without sacrificing volume.
