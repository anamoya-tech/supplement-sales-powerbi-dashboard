# Supplement Sales — Power BI Dashboard (Data Quality + Revenue Audit)

## Overview
This project builds an executive-ready Power BI dashboard to analyze e-commerce supplement sales performance by **country**, **platform**, and **category**, while also validating **data quality** signals (issues and revenue mismatches).

The focus is not only visualization, but **trustworthy reporting**: KPIs are built with DAX measures and designed to be filter-aware.

## Business Questions
- How does total revenue evolve over time (monthly)?
- Do revenue and units move together (volume vs pricing/discount effects)?
- Which countries and platforms drive revenue?
- Which categories lead by **units** vs **revenue** (and do they differ)?
- How do discounts relate to revenue performance?
- What is the return rate by segment?
- Are there data quality issues or revenue mismatches impacting results?

## KPI Header (Current Snapshot)
- Revenue Total: **$23M**
- Units Sold: **658K**
- Return Rate: **1.01%**
- Avg Discount: **12.4%**
- Issue Rate: **0.0%**
- Revenue Mismatch Rate: **0.0%**

> Note: Issue and mismatch rates currently show 0%, which indicates either a clean dataset or non-populated flags. This is explicitly tracked as part of the audit layer.

## Data & Model
- Single fact table (`clean_data`) with cleaned dimensions and metrics:
  - `date_clean`, `location_clean`, `platform_clean`, `category_clean`
  - `revenue_clean`, `units_sold_clean`, `units_returned_clean`, `discount_clean`
  - audit flags: `issue_flag`, `revenue_mismatch_flag`, etc.
- Time axis standardized with `MonthYear_EN` + `MonthYearSort`.

## Key DAX Measures
- Revenue Total
- Units Sold / Units Returned
- Return Rate
- Avg Discount
- Issue Rate
- Revenue Mismatch Rate

## How to Run
1. Download the `.pbix` file from `/powerbi/`.
2. Open in **Power BI Desktop**.
3. If needed, update the data source path to the cleaned dataset.

## Screenshots
- KPI header preview: `/assets/kpi_header.png`
- Full dashboard preview: `/assets/dashboard_preview.png`

## Next Steps
- Add monthly trend visuals (Revenue + Units)
- Country/platform breakdown
- Category ranking toggle (Units vs Revenue)
- Discount vs revenue relationship (scatter)
- Returns analysis by segment
