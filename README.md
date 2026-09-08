<!-- PROJECT 4 README — Supply Chain Demand Analytics -->

<div align="center">

# 📦 Supply Chain Performance & Demand Analytics

### *From Purchase Order to Customer Delivery — Measured, Analyzed, Optimized*

<br/>

![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-Public-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-Portfolio-181717?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active-00C853?style=for-the-badge)

<br/>

![Tables](https://img.shields.io/badge/7%20Tables-Relational%20Schema-764ba2?style=flat-square&logoColor=white)
![Rows](https://img.shields.io/badge/5%2C380%20Rows-Live%20Dataset-667eea?style=flat-square)
![Queries](https://img.shields.io/badge/14%20SQL%20Queries-L1%20to%20L3-f093fb?style=flat-square)
![Role](https://img.shields.io/badge/Target%20Role-Supply%20Chain%20Analyst-E97627?style=flat-square)

</div>

---

<div align="center">

## 💬 The Question Every Supply Chain Analyst Gets Asked

</div>

> *"Walk me through how you would measure the health of an end-to-end supply chain."*

Most candidates talk about spreadsheets and gut feel. This project is my answer — built in SQL and Tableau, covering every stage from supplier purchase order to customer delivery.

---

<div align="center">

## 🗺️ The Supply Chain Cycle This Project Covers

</div>

```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│  SUPPLIERS  │────▶│  PURCHASE   │────▶│  INBOUND    │────▶│  WAREHOUSE  │
│             │     │   ORDERS    │     │  FREIGHT    │     │  INVENTORY  │
│ Scorecard   │     │ OTD & Delay │     │ Cost & Time │     │ Stock Levels│
└─────────────┘     └─────────────┘     └─────────────┘     └──────┬──────┘
                                                                   │
                                                                   │
┌─────────────┐     ┌─────────────┐     ┌─────────────┐            │
│     KPI     │     │   DEMAND    │     │    SALES    │◀───────────┘
│  DASHBOARD  │     │ FORECASTING │     │   ORDERS    │
│ 10 Metrics  │     │ Accuracy %  │     │Revenue + P&L│
└─────────────┘     └─────────────┘     └─────────────┘
```

---

<div align="center">

## 🔬 What Makes This Project Different From My Others

</div>

<table>
<thead>
<tr>
<th>Dimension</th>
<th>Projects 1–3</th>
<th>Project 4</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>Industry angle</b></td>
<td>Freight forwarding & 3PL</td>
<td>Retail & manufacturing supply chain</td>
</tr>
<tr>
<td><b>Business focus</b></td>
<td>Carrier performance & routing</td>
<td>Full cycle — supplier to customer</td>
</tr>
<tr>
<td><b>Unique table</b></td>
<td>Route optimization before/after</td>
<td>KPI targets vs actuals — traffic light</td>
</tr>
<tr>
<td><b>New concept</b></td>
<td>D&D charges, transshipment fees</td>
<td>Demand forecasting, Pareto analysis</td>
</tr>
<tr>
<td><b>Analytics depth</b></td>
<td>Operational metrics</td>
<td>P&L, gross margin, revenue ranking</td>
</tr>
</tbody>
</table>

---

<div align="center">

## 📋 The 14 Business Questions

</div>

<details>
<summary><b>🔵 Level 1 — Foundational Supply Chain Analysis (click to expand)</b></summary>

<br/>

| # | Question | SQL Technique | Business Value |
|---|---|---|---|
| Q1 | Which suppliers score best across OTD, quality and compliance? | Calculated column, ORDER BY | Replaces gut-feel with ranked scorecard |
| Q2 | What % of POs arrive on time vs delayed? | CASE WHEN, window % | Quantifies procurement reliability |
| Q3 | Which SKUs are critically low right now? | WHERE filter, multi-column sort | Prevents stockouts before they happen |
| Q4 | Which categories drive the most revenue and margin? | GROUP BY quarter, aggregations | Identifies where to focus buying effort |
| Q5 | Where is our demand forecast least accurate? | GROUP BY category, variance calc | Improves planning inputs |

</details>

<details>
<summary><b>🟡 Level 2 — CTEs, Joins & Subqueries (click to expand)</b></summary>

<br/>

| # | Question | SQL Technique | Business Value |
|---|---|---|---|
| Q6 | Do high risk suppliers actually deliver late more often? | CTE + JOIN | Validates risk ratings with real data |
| Q7 | Which SKUs need ordering before stock runs out in lead time? | CTE + JOIN + CASE WHEN | Prevents stockout during replenishment |
| Q8 | How much revenue are we losing to stockouts? | JOIN + lost revenue calc | Attaches a dollar value to stock failures |
| Q9 | Which freight shipments cost significantly above average? | Correlated subquery | Flags outliers for cost review |
| Q10 | How is monthly revenue and gross profit trending? | Running total window function | Executive P&L visibility |

</details>

<details>
<summary><b>🔴 Level 3 — Window Functions & Executive Scorecard (click to expand)</b></summary>

<br/>

| # | Question | SQL Technique | Business Value |
|---|---|---|---|
| Q11 | Which SKUs make up 80% of revenue — Pareto? | RANK() + cumulative % OVER | Focus buying on top revenue drivers |
| Q12 | Who is the best supplier in each product category? | RANK() PARTITION BY category | Category-level sourcing decisions |
| Q13 | Are we hitting our monthly KPI targets? | RANK() OVER best month | Executive dashboard input |
| Q14 | Full supply chain health scorecard per supplier | Triple nested CTE + RANK() | One view — every risk factor combined |

</details>

---

<div align="center">

## 🗄️ Database Schema

</div>

| Table | Rows | Description |
|---|---|---|
| `p4_suppliers` | 20 | Scorecard — OTD %, quality, compliance, lead time, risk rating |
| `p4_purchase_orders` | 1,000 | POs with order qty, value, delay days, on-time flag |
| `p4_inventory` | 120 | 30 SKUs × 4 warehouses — stock, reorder points, days of supply |
| `p4_demand_forecast` | 1,080 | Monthly forecast vs actual by SKU — accuracy % and revenue impact |
| `p4_sales_orders` | 2,000 | Revenue, COGS, gross profit, fulfillment rate, backorders |
| `p4_freight_shipments` | 800 | Inbound shipments linking POs to inventory — cost and delay |
| `p4_kpi_targets` | 360 | 10 KPIs × 36 months — target, actual, variance, traffic light status |

**Foreign keys:** `Supplier_ID` links suppliers → purchase orders → inventory → freight. `SKU_ID` links inventory → demand forecast → sales orders.

---

<div align="center">

## 🏭 Dataset Scope

</div>

<table>
<tr>
<td align="center" width="25%">

**30 SKUs**
Electronics · Furniture
Apparel · Appliances
Sports · Health · Kitchen

</td>
<td align="center" width="25%">

**4 Warehouses**
Toronto DC
Vancouver DC
Montreal DC
Calgary DC

</td>
<td align="center" width="25%">

**20 Customers**
Walmart Canada
Canadian Tire
Costco · IKEA
Loblaw · Best Buy

</td>
<td align="center" width="25%">

**10 KPIs**
OTD Rate · Forecast Accuracy
Inventory Turnover
Fulfillment Rate
Gross Margin · and more

</td>
</tr>
</table>

---

<div align="center">

## 📁 Repository Structure

</div>

```
supply-chain-demand-analytics/
│
├── 📂 data/
│   ├── p4_suppliers.csv              # 20 supplier scorecards
│   ├── p4_purchase_orders.csv        # 1,000 purchase orders with delay data
│   ├── p4_inventory.csv              # 120 SKU × warehouse stock records
│   ├── p4_demand_forecast.csv        # 1,080 monthly forecast vs actual
│   ├── p4_sales_orders.csv           # 2,000 orders with revenue and margin
│   ├── p4_freight_shipments.csv      # 800 inbound shipments with cost
│   └── p4_kpi_targets.csv            # 360 monthly KPI records
│
├── 📂 queries/
│   └── supply_chain_analytics.sql    # All 14 SQL queries — L1 through L3
│
└── README.md
```

---

<div align="center">

## 🗺️ Project Roadmap

</div>

- [x] Design 7-table end-to-end supply chain schema
- [x] Generate 5,380 rows of realistic Canadian retail data
- [x] Load all tables into MySQL with validated row counts
- [x] Write Level 1 queries — foundational supply chain analysis
- [x] Write Level 2 queries — CTEs, joins and subqueries
- [x] Write Level 3 queries — window functions and executive scorecard
- [ ] Build Tableau dashboard
- [ ] Write case study

---

<div align="center">

## 📂 Full Portfolio

| Project | Focus | Tables | Dashboard |
|:---:|---|:---:|:---:|
| [**01**](https://github.com/Jaspreet-analyst/ocean-freight-sql-analytics) | Ocean Freight SQL Analytics | 1 | ✅ Live |
| [**02**](https://github.com/Jaspreet-analyst/supply-chain-risk-analytics) | Supply Chain Risk & Cost Analytics | 5 | ✅ Live |
| [**03**](https://github.com/Jaspreet-analyst/freight-performance-analytics) | Global Freight Performance & Customer Impact | 7 | ✅ Live |
| [**04**](https://github.com/Jaspreet-analyst/supply-chain-demand-analytics) | Supply Chain Performance & Demand Analytics | 7 | 🔄 In Progress |

<br/>

**Jaspreet Singh** · Ocean Import Coordinator · CEVA Logistics · Greater Toronto Area

CIFFA Certified · FIATA Diploma · Six Sigma Green Belt · Scrum Master (CSM)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jaspreet-singh-5b13b510b/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jaspreet-analyst)
[![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/jaspreet.singh5400/vizzes)

</div>
