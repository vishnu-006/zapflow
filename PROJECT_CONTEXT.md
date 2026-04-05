```markdown
# ZapFlow — Quick Commerce Data Platform
## Project Context & Progress Tracker

---

## Goal
A production-grade Data Engineering portfolio project built entirely 
on Databricks Community Edition. Simulates a quick commerce platform 
(Zepto/Blinkit style) with end-to-end data pipeline covering 
ingestion, transformation, modeling, quality checks, and serving layer.


## Tech Stack
| Layer | Tool |
|---|---|
| Processing | Databricks (Community Edition) |
| Storage | Databricks DBFS / Delta Lake |
| Format | Delta Tables |
| Orchestration | Databricks Workflows |
| Quality Checks | Custom DQ framework |
| Serving | Databricks SQL / Power BI Desktop |
| Version Control | GitHub |
| Language | PySpark + Python |

---

## Architecture
```
Simulation Scripts (Python)
        ↓
   Bronze Layer (Raw Delta tables — no transformations)
        ↓
   Silver Layer (Cleaned, typed, deduplicated, DQ flagged)
        ↓
   Gold Layer (Star schema — facts and dimensions)
        ↓
   Serving Layer (Aggregated views / Power BI)
```

---

## 5 Data Domains
| Domain | Key Challenge |
|---|---|
| Customers | SCD Type 2, segmentation |
| Dark Stores | Location master, capacity tracking |
| Inventory | Daily snapshots, stock depletion patterns |
| Orders | Incremental loads, deduplication, peak hour patterns |
| Deliveries | SLA breach detection, late data handling |

---

## Notebook Structure
```
zapflow/
├── 01_simulation/
│   ├── 01_generate_customers
│   ├── 02_generate_dark_stores
│   ├── 03_generate_inventory
│   ├── 04_generate_orders
│   └── 05_generate_deliveries
├── 02_bronze/
├── 03_silver/
├── 04_gold/
├── 05_quality_checks/
├── 06_workflows/
└── README.md
```

---

## Progress Tracker
### Phase 1 — Data Simulation
- [ ] 01_generate_customers
- [ ] 02_generate_dark_stores
- [ ] 03_generate_inventory
- [ ] 04_generate_orders
- [ ] 05_generate_deliveries

### Phase 2 — Bronze Layer
- [ ] bronze_customers
- [ ] bronze_dark_stores
- [ ] bronze_inventory
- [ ] bronze_orders
- [ ] bronze_deliveries

### Phase 3 — Silver Layer
- [ ] silver_customers (SCD Type 2)
- [ ] silver_dark_stores
- [ ] silver_inventory
- [ ] silver_orders (dedup + incremental)
- [ ] silver_deliveries (SLA calculation)

### Phase 4 — Gold Layer
- [ ] dim_customers
- [ ] dim_dark_stores
- [ ] dim_dates
- [ ] fact_orders
- [ ] fact_deliveries
- [ ] gold_order_summary
- [ ] gold_sla_breach_report
- [ ] gold_inventory_health

### Phase 5 — Quality Checks
- [ ] DQ framework notebook
- [ ] DQ rules per domain

### Phase 6 — Workflows & Orchestration
- [ ] End-to-end Databricks Workflow

### Phase 7 — Documentation
- [ ] Architecture diagram
- [ ] README.md
- [ ] Interview talking points per component

---

## Key Decisions & Why
| Decision | Reason |
|---|---|
| Delta Lake over Parquet | ACID transactions, time travel, schema enforcement |
| Simulated data over Kaggle | Full control over quality issues and patterns |
| Single project over multiple | Depth > breadth for senior interviews |
| Community Edition only | Zero cost, realistic constraint |
| Quick Commerce domain | Modern, relatable, not oversaturated |

---


