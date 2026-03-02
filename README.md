# 🏎️ Motorsport Operations and Strategy Business Analysis

A full-stack Business Intelligence project analyzing Formula 1 team performance across **Management, Engineering, and Operations** using PostgreSQL and Power BI.

This repository demonstrates an end-to-end analytics workflow:
- Data sourcing
- Dimensional modeling (Star Schema)
- KPI engineering in SQL
- Field benchmarking using DAX
- Executive dashboard development

---

# 📂 Repository Structure

```
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

---

# 🎯 Project Objective

This project evaluates strategic motorsport performance by answering:

- Are teams spending efficiently?
- Does engineering consistency drive reliability?
- How does operational execution impact results?
- What trade-offs exist between cost, performance, and stability?

The solution integrates financial, technical, and operational KPIs into a unified analytical framework.

---

# 🛠️ Tech Stack

- **PostgreSQL** — Data modeling and KPI view creation
- **SQL** — Star schema design and aggregations
- **Power BI** — Multi-page dashboard development
- **DAX** — Selected vs Field benchmarking logic

---

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

---

# 📊 Dashboard Overview

The Power BI report contains three analytical layers:

---

## 1️⃣ Management Overview

![Management Overview](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Dashboard/Dashboard%20Preview/Management_Overview.png)

Focus:
- Cost per Point trend
- Reliability vs Scoring
- Financial efficiency benchmarking

Provides macro-level executive insights.

---

## 2️⃣ Engineering Performance Insights

![Engineering Performance Insights](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Dashboard/Dashboard%20Preview/Engineering_Performance_Insights.png)

Focus:
- Average Lap Time trend
- Lap Time Volatility (Std Dev)
- Reliability vs Consistency trade-off
- Team-level benchmarking

Isolates technical performance drivers.

---

## 3️⃣ Operations Overview

![Operations Overview](https://github.com/MayankAgrawal099/Motorsport_Operations_and_Strategy_Business_Analysis/blob/main/Dashboard/Dashboard%20Preview/Operations_Overview.png)

Focus:
- Average Pit Time trend
- Pit Stop consistency
- Failure rate analysis
- Operational efficiency comparison

Evaluates race execution discipline.

---

# 🧠 Analytical Architecture

The project implements:
- Star schema modeling
- Selected Team vs Field Average benchmarking
- Gap measures (Selected – Field)
- Multi-season trend analysis
- Trade-off visualization
- Dynamic slicer-based filtering

---

# 📈 Key Concepts Demonstrated

- Dimensional data modeling
- Performance benchmarking
- Cost-efficiency evaluation
- Strategic trade-off analysis
- Executive dashboard storytelling
- Advanced DAX measure engineering

---

# ⚠️ Notes

- Dataset source: Kaggle (F1 World Championship dataset)
- Cost values are modeled assumptions for analytical simulation
- This project is built for educational and portfolio demonstration purposes

---

# 📊 Business Findings

The analytical model reveals several strategic insights:

### 1️⃣ Cost Efficiency Improved Post Hybrid Era
Cost per point decreased steadily after 2016, suggesting improved development allocation efficiency across teams.

### 2️⃣ Lap Consistency Strongly Correlates With Reliability
Teams with lower lap time volatility consistently demonstrate higher reliability scores and improved points per race.

### 3️⃣ Operational Stability Impacts Scoring
Higher pit time volatility is associated with increased failure rates and reduced competitive positioning.

### 4️⃣ High Spending Does Not Guarantee Performance
Certain teams demonstrate above-field cost per point without proportional gains in scoring efficiency.

### 5️⃣ Trade-Off Between Aggressive Performance and Stability
Teams optimizing for lap time often experience reliability risk, indicating a balance between peak performance and durability.

These findings illustrate the strategic tension between cost, engineering performance, and operational execution.

---

# 👨‍💻 Author

Mayank Anil Agrawal