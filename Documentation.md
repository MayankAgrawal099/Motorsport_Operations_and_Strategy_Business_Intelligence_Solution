# 📘 Technical Documentation  
## Motorsport Operations and Strategy Business Analysis

This document explains the technical architecture, modeling logic, KPI calculations, and analytical design decisions behind the project.

---

# 1️⃣ Data Source

Dataset:  
F1 World Championship Dataset (Kaggle)

The dataset contains race results, lap times, constructors, drivers, pit stops, and standings data.

Cost values are modeled assumptions introduced for strategic performance simulation.

---

# 2️⃣ Data Architecture

The project follows a **Star Schema design**.

## Core Components

### Dimension Tables
- `dim_constructor`
- `dim_race`
- `dim_season`

### Fact Tables
- `fact_race_results`
- `fact_lap_times`
- `fact_pit_stops`

### Analytical Views
- `public_vw_management_kpis`
- `public_vw_engineering_kpis`
- `public_vw_operations_kpis`

---

# 3️⃣ SQL Workflow Structure

The SQL pipeline is executed sequentially:

## 01_schema_setup.sql
Creates base tables and schema structure.

## 02_data_validation.sql
Ensures no null inconsistencies or incorrect joins.

## 03_dimension_tables.sql
Builds cleaned dimension tables.

## 04_fact_tables.sql
Aggregates race-level, lap-level, and pit-level metrics.

## 05_cost_assumptions.sql
Introduces cost modeling for performance simulation.

## 06_kpi_views.sql
Creates analytical KPI views for Power BI consumption.

## 07_final_checks.sql
Validates record counts and aggregation consistency.

---

# 4️⃣ Power BI Model Design

Power BI connects directly to PostgreSQL views.

Relationships:
- `dim_constructor` → Fact tables (1:* relationship)
- `dim_race` → Fact tables (1:* relationship)

The model supports slicer-driven filtering across all dashboards.

---

# 5️⃣ KPI Engineering Logic

Each KPI follows a 3-measure structure:

• Selected Team Measure  
• Field Average Measure  
• Gap Measure (Selected - Field)

Example:
• Selected AVG Lap Time
• Field ANG Lap Time
• Lap Time Gap

This enables dynamic benchmarking against the field.

---

# 6️⃣ Analytical Themes

The project is structured across three business layers:

## Management Layer
Focus: Financial efficiency and scoring ROI.

Metrics:
- Total Cost
- Cost per Point
- Reliability Score

## Engineering Layer
Focus: Car performance and consistency.

Metrics:
- Average Lap Time
- Lap Time Std Dev
- Points per Race

## Operations Layer
Focus: Race execution stability.

Metrics:
- Average Pit Time
- Pit Time Volatility
- Failure Rate

---

# 7️⃣ Strategic Analysis Framework

The dashboards enable:

- Field benchmarking
- Multi-season trend analysis
- Trade-off mapping
- Gap identification
- Executive decision support

---

# 8️⃣ Assumptions & Limitations

- Cost data is simulated for modeling purposes.
- Dataset spans historical seasons.
- Results are aggregated at season level for comparability.
- Real-world team budgets are not directly sourced.

---

# 9️⃣ Future Enhancements

- Budget cap era analysis
- Driver-level impact modeling
- Predictive scoring regression model
- Monte Carlo reliability simulation