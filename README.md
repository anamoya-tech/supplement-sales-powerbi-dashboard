# Supplement Sales — Power BI Dashboard  
**Revenue Analysis & Data Quality Validation**

## Overview
This project presents an **executive-ready Power BI dashboard** built on top of a cleaned e-commerce dataset of nutritional supplement sales.

The goal is to analyze **commercial performance** (revenue, units, returns, discounts) by **country, platform, and category**, while also validating **data quality signals** to ensure the reliability of the analysis.

This dashboard is intentionally designed to reflect a **real business reporting scenario**, prioritizing clear KPIs, filter-aware DAX measures, and decision-oriented visuals.

---

## Related Project: Data Cleaning & Quality Audit
The dataset used in this dashboard was previously assessed, cleaned, and audited in a separate project:

🔗 **Data Cleaning & Quality Audit (Google Sheets)**  
https://github.com/anamoya-tech/supplement-sales-data-quality

That project documents:
- Data quality checks
- Cleaning decisions
- Issue and mismatch flag logic
- BEFORE vs AFTER validation metrics

This Power BI dashboard builds directly on the **cleaned output** of that pipeline.

---

## Business Questions Addressed
- What is the overall revenue and sales volume performance?
- How do revenue and units behave together (volume vs pricing effects)?
- What is the average discount level across sales?
- What is the return rate?
- Are there any data quality issues or revenue mismatches that could affect trust in the analysis?

---

## KPI Snapshot (Current View)
The dashboard opens with a KPI header designed for executive consumption:

- **Revenue Total:** $23M  
- **Units Sold:** 658K  
- **Return Rate:** 1.01%  
- **Avg Discount:** 12.4%  
- **Issue Rate:** 0.0%  
- **Revenue Mismatch Rate:** 0.0%

> Issue and mismatch rates currently show 0%, indicating either a clean dataset or non-populated flags.  
> These metrics are intentionally included to make **data reliability explicit**.

---

## Data Model & Design
- Single cleaned fact table (`clean_data`)
- Core dimensions:
  - Date (standardized monthly axis)
  - Country
  - Platform / Store
  - Product category
- Core metrics:
  - Revenue
  - Units sold
  - Units returned
  - Discount
- Audit flags:
  - Issue flags
  - Revenue mismatch flags

All KPIs are implemented as **DAX measures**, ensuring correct aggregation and responsiveness to filters.

---

## Tools & Skills Demonstrated
- Power BI Desktop
- DAX (measures, ratios, defensive calculations)
- KPI design and executive reporting
- Data quality awareness in BI
- Clean dashboard layout and formatting
- Business-first analytical thinking

---

## Project Structure
├─ powerbi/
│  └─ supplement_sales_dashboard.pbix
├─ assets/
│  ├─ kpi_header.png
│  ├─ revenue_monthly.png
│  ├─ Revenue_vs_Units_Monthly.png
│  ├─ Revenue_quarterly.png
│  └─ Revenue_vs_Units_Quarterly.png
└─ README.md


---

## Next Steps
Planned extensions of the dashboard include:
- Monthly revenue and units trend analysis
- Country and platform performance comparison
- Category ranking (Units vs Revenue)
- Discount vs revenue relationship analysis
- Returns analysis by segment

---

## Phase 1 — Performance (Completed)
Phase 1 focuses on overall performance and trend validation:

- **Revenue over time (Monthly):** monthly trend view for seasonality and changes.
- **Revenue vs Units (Monthly):** comparison to assess whether performance is volume-driven or pricing-driven.
- **Quarterly views:** additional quarterly versions were created to reduce noise and improve readability.

**Key takeaway:** Revenue and Units Sold move consistently over time, suggesting performance is primarily **volume-driven** rather than driven by pricing distortions.

---

## Screenshots

### KPI Overview
High-level executive KPIs summarizing overall commercial performance and data quality signals.

![KPI Header](assets/kpi_header.png)

---

### Revenue Over Time (Monthly)
Monthly revenue trend used to identify seasonality, fluctuations, and overall performance evolution.

![Monthly Revenue](assets/revenue_monthly.png)

---

### Revenue vs Units Sold (Monthly)
Comparison between revenue and units sold at a monthly level to assess whether growth is driven by volume or pricing effects.

![Revenue vs Units Monthly](assets/Revenue_vs_Units_Monthly.png)

---

### Revenue Over Time (Quarterly)
Quarterly aggregation of revenue to reduce noise and highlight structural trends.

![Quarterly Revenue](assets/Revenue_quarterly.png)

---

### Revenue vs Units Sold (Quarterly)
Clean quarterly comparison of revenue and units sold, enabling a clearer assessment of volume-driven performance.

![Revenue vs Units Quarterly](assets/Revenue_vs_Units_Quarterly.png)


---
## Notes
This project is part of a broader portfolio focused on **end-to-end data analysis**, from data quality assessment to BI-ready reporting.
