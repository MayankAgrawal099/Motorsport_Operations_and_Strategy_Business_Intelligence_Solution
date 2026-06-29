# 🏎️ Motorsport Operations and Strategy Business Intelligence Solution

## Executive Summary

This repository presents an end-to-end **Business Intelligence
solution** built around Formula 1 motorsport data. Rather than serving
as a dashboard-only project, it demonstrates how raw operational data
can be transformed into executive decision support through an
enterprise-inspired analytics pipeline.

The solution integrates PostgreSQL, SQL, dimensional modeling, Power BI,
and DAX to evaluate financial efficiency, engineering consistency,
operational execution, and strategic trade-offs across Formula 1
constructors.

The analytical architecture follows a layered BI approach:

**Raw Data → PostgreSQL → Analytical Data Warehouse → Business Logic
Layer → Semantic Model → Executive Decision Support**

### Project Highlights

-   End-to-end Business Intelligence architecture
-   PostgreSQL analytical data warehouse
-   Star schema dimensional model
-   SQL-driven KPI engineering
-   Interactive Power BI semantic model
-   Executive decision support dashboards
-   Motorsport strategy and operations analytics

------------------------------------------------------------------------

# 📊 Dashboard Preview

> **Dashboard screenshots will be added here.**

### Management Overview

![Management Overview](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Dashboard/Dashboard%20Preview/Management_Overview.png)


------------------------------------------------------------------------

### Engineering Performance Insights

![Engineering Performance Insights](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Dashboard/Dashboard%20Preview/Engineering_Performance_Insights.png)

------------------------------------------------------------------------

### Operations Overview

![Operations Overview](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Intelligence_Solution/blob/main/Dashboard/Dashboard%20Preview/Operations_Overview.png)

------------------------------------------------------------------------

# 🏗️ Solution Architecture

![Architecture Diagram](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Diagram/Architecture_Diagram_Preview.png)

The architecture separates data storage, business logic, semantic modeling, and visualization into independent layers. This mirrors enterprise Business Intelligence systems, ensuring scalability, maintainability, and consistent KPI definitions across all dashboards.

This solution follows a layered Business Intelligence architecture
inspired by enterprise analytics platforms.

  -----------------------------------------------------------------------
  Layer                 Responsibility
  --------------------- -------------------------------------------------
  Raw Motorsport        Source data ingestion
  Dataset               

  PostgreSQL            Data storage, cleansing, validation,
                        normalization

  Analytical Data       Dimensional modeling using a Star Schema
  Warehouse             

  Business Logic Layer  KPI engineering, aggregations and analytical SQL
                        views

  Power BI Semantic     Relationships, DAX measures and calculations
  Model                 

  Executive Decision    Interactive dashboards for strategic decision
  Support               making
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# 🎯 Business Problem

Modern motorsport organizations generate massive volumes of operational,
engineering, and performance data. While race results provide outcomes,
they rarely explain *why* teams consistently succeed or fail.

Decision-makers require an integrated analytical solution capable of
answering questions such as:

-   Which teams convert investment into championship points most
    efficiently?
-   Does engineering consistency correlate with competitive performance?
-   How does operational execution influence race outcomes?
-   Which strategic trade-offs maximize competitive advantage?
-   Where should management prioritize future investment?

This project addresses these challenges by transforming historical
Formula 1 data into an executive-ready Business Intelligence solution.

------------------------------------------------------------------------

# ⭐ Key Features

-   Executive Decision Support dashboards
-   Enterprise-inspired analytical architecture
-   Star Schema dimensional data warehouse
-   SQL-centric Business Logic Layer
-   KPI engineering using PostgreSQL
-   Interactive Power BI Semantic Model
-   Dynamic benchmarking with DAX
-   Multi-season strategic analysis

### Engineered KPIs

-   Cost per Point
-   Reliability Score
-   Failure Rate
-   Average Lap Time
-   Lap Time Volatility
-   Average Pit Time
-   Pit Stop Consistency
-   Performance Benchmarking

------------------------------------------------------------------------

# 🗄️ ER Diagram / Semantic Data Model

![ER Diagram](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Diagram/ER_Diagram.png)

The solution adopts a Star Schema optimized for analytical workloads.

### Dimension Tables

-   Dim Constructor
-   Dim Race

### Analytical Fact Tables

-   Management Intelligence
-   Engineering Intelligence
-   Operations Intelligence
-   Strategic Trade-off Analysis

The semantic model uses one-to-many relationships to ensure consistent
filtering, KPI aggregation, and cross-dashboard analysis.

------------------------------------------------------------------------

# 🛠️ Technology Stack

| Technology | Role | Why it was Chosen |
|------------|------|-------------------|
| **PostgreSQL** | Analytical Data Warehouse | Chosen as the central repository for storing, validating, and transforming raw motorsport data into an optimized analytical model. Its support for advanced SQL, relational integrity, and scalable querying makes it well suited for Business Intelligence workflows. |
| **SQL** | Business Logic & KPI Engineering | Used to centralize business logic, create dimension and fact tables, engineer KPIs, and build analytical views. This ensures the database serves as the single source of truth before data reaches the reporting layer. |
| **Power BI** | Semantic Modeling & Visualization | Selected for its enterprise-grade semantic modeling, interactive dashboards, and seamless integration with PostgreSQL. It enables business users to explore insights through dynamic filtering and executive reporting. |
| **DAX** | Dynamic Calculations | Used to develop context-aware measures, dynamic benchmarks, and advanced KPIs that automatically adapt to user selections and report filters. |
| **Power Query** | Data Ingestion & Transformation | Utilized to connect with PostgreSQL, perform lightweight data shaping, and prepare the semantic model while keeping major transformations within the SQL layer. |
| **Git & GitHub** | Version Control & Collaboration | Used to manage source code, track project evolution, maintain comprehensive documentation, and present the complete Business Intelligence solution as a professional portfolio project. |
| **Kaggle Formula 1 Dataset** | Source Data | Chosen for its comprehensive historical Formula 1 data, including constructors, races, lap times, pit stops, and results, providing a realistic foundation for analytical modeling and KPI engineering. |

------------------------------------------------------------------------

# 📂 Repository Structure

``` text
Motorsport_Operations_and_Strategy_Business_Analysis/
│
├── Dataset/
│ ├── constructors.csv
│ ├── lap_times.csv
│ ├── pit_stops.csv
│ ├── races.csv
│ ├── results.csv
│ ├── seasons.csv
| ├── status.csv
│ └── README.md
|
├── SQL_Analysis/
│ ├── 01_schema_setup.sql
│ ├── 02_data_validation.sql
│ ├── 03_dimension_tables.sql
│ ├── 04_fact_tables.sql
│ ├── 05_cost_assumptions.sql
│ ├── 06_kpi_views.sql
│ ├── 07_final_checks.sql
│ └── README.md
│
├── Diagram/
│   ├── Architecture_Diagram_Preview.png
│   ├── Architecture_Diagram.drawio
│   └── ER_Diagram.png
│
├── Dashboards/
│ ├── Motorsport_Dashboard.pbix
│ ├── Dashboard Preview/
│ │ ├── Management_Overview.png
│ │ ├── Engineering_Performance_Insights.png
│ │ └── Operations_Overview.png
│ └── README.md
│
├── Documentation.md
└── README.md
```

The repository is organized to mirror a real-world Business Intelligence
workflow where SQL acts as the **single source of truth**, while Power
BI functions as the executive presentation layer.

------------------------------------------------------------------------

# 📈 Dashboard Pages

## Executive Overview

Provides management-level visibility into financial efficiency,
championship performance, and strategic benchmarking.

**Primary KPIs**

-   Total Cost
-   Cost per Point
-   Reliability Score
-   Championship Points
-   Team Benchmarking

------------------------------------------------------------------------

## Engineering Intelligence

Evaluates technical consistency and engineering competitiveness.

**Primary KPIs**

-   Average Lap Time
-   Lap Time Standard Deviation
-   Reliability Trend
-   Performance Benchmark

------------------------------------------------------------------------

## Operations Intelligence

Measures operational execution throughout the season.

**Primary KPIs**

-   Average Pit Time
-   Pit Stop Consistency
-   Failure Rate
-   Operational Efficiency

------------------------------------------------------------------------

# 📊 Business Findings

### Financial efficiency outweighs absolute spending

Higher expenditure does not consistently produce stronger championship
performance. Efficient allocation of resources delivers greater
competitive value.

### Engineering consistency improves competitive outcomes

Lower lap-time variability strongly correlates with improved reliability
and sustained championship performance.

### Operational excellence creates measurable advantage

Consistent pit-stop execution and lower failure rates contribute
directly to improved race outcomes.

### Reliability drives long-term competitiveness

Mechanical consistency has a greater influence on sustained success than
isolated peak performance.

### Strategic trade-offs are quantifiable

The solution enables management to evaluate the balance between
investment, engineering capability, and operational execution to
identify areas with the highest potential return.

------------------------------------------------------------------------

# 🚀 Future Improvements

-   Driver-level intelligence
-   Budget Cap era analytics
-   Predictive race outcome modeling
-   Reliability forecasting using Machine Learning
-   Monte Carlo race strategy simulation
-   Live Formula 1 API integration
-   Automated ETL pipelines
-   Power BI Service deployment
-   CI/CD dashboard publishing

------------------------------------------------------------------------

# 🚀 How To Run This Project

Follow these steps to fully reproduce the project.

---

## Step 1 — Download Dataset

1. Download the F1 dataset from Kaggle:

   https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020

2. Extract all required CSV files.
3. Place them inside the `Dataset/` folder.

---

## Step 2 — Setup PostgreSQL

1. Install PostgreSQL.
2. Create a new database:

```sql
CREATE DATABASE motorsport_analysis;
```

3. Connect to the database.

---

## Step 3 - Execute SQL Scripts (In Order)

Navigate to SQL_Analysis/ and execute the files sequentially:

1. 01_schema_setup.sql
2. 02_data_validation.sql
3. 03_dimension_tables.sql
4. 04_fact_tables.sql
5. 05_cost_assumptions.sql
6. 06_kpi_views.sql
7. 07_final_checks.sql

These scripts will:
- Create the star schema
- Build dimension and fact tables
- Generate KPI views used in Power BI

---

## Step 4 — Open Power BI Dashboard

1. Open:
Dashboards/Motorsport_Dashboard.pbix
2. Update database connection:
- Server: localhost
- Database: motorsport_analysis
3. Click Refresh

All dashboards will load from the SQL views.

------------------------------------------------------------------------

## Skills Demonstrated

• Business Intelligence

• SQL Development

• PostgreSQL

• Star Schema Design

• Data Modeling

• ETL

• KPI Engineering

• Power BI

• DAX

• Dashboard Design

• Executive Reporting

• Business Analytics

------------------------------------------------------------------------

# 👨‍💻 Author

**Mayank Anil Agrawal**

Aspiring Business Intelligence & Data Analyst specializing in SQL,
PostgreSQL, Power BI, Data Modeling, and Business Intelligence.
