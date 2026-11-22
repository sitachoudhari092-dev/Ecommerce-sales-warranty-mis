# Ecommerce-sales-warranty-mis
MS Excel E-Commerce MIS report analyzing 10,000+ orders, lifecycle rates, monthly trends, revenue leakage, and warranty/support lookup rules

# E-Commerce Sales & Warranty MIS Dashboard (MS Excel)

## Overview
An MIS workbook built in **Microsoft Excel** using a **10,000+ row** global e-commerce sales dataset (`rawdata`) enriched with a lookup reference sheet (`product rule`). It tracks order lifecycle status rates, monthly trends, revenue leakage, and warranty/support rules across product categories.

## Dataset & Lookup Enrichment Notes
- **Source Dataset:** 10,000+ row global e-commerce dataset (`rawdata`) containing order dates, product categories/items, order statuses (`Delivered`, `Returned`, `Cancelled`, `Processing`), and revenue/cost fields.
- **Lookup Rules & Controls (`product rule`):** Created a reference rules sheet and used `VLOOKUP` to pull `Warranty_Months`, `Support_Team`, and `Support_Region` onto `rawdata`, alongside **Data Validation** rules and a **Slicer** (`Warranty_Months`) for interactive filtering.
- **Metric Adaptation:** Because the raw dataset provides order statuses and revenue rather than separate warranty claim logs or repair bills, post-purchase friction and financial leakage are measured via order lifecycle rates (`Delivered %`, `Returned %`, `Cancelled %`, `Processing %`), **Lost Revenue** (`Returned` + `Cancelled` revenue), and **Revenue Loss %**.

## Key Findings & MIS Takeaways
- **Books & Media:** Highest overall order volume.
- **Clothing:** Highest **Return Rate %** (`21%`) and highest **Processing Rate %**, pointing to sizing/fit friction and order-processing/fulfillment delays.
- **Home & Kitchen:** Highest **Cancellation Rate %**, warranting checks on stock availability and pre-shipment delays.
- **Beauty & Health:** Leads **Delivery Success Rate %**, yet still shows notable **Revenue Loss %** on affected orders.
- **Electronics:** Generates the highest **Delivered** revenue while also leading total **Lost Revenue** and sharing the top **Revenue Loss %**, highlighting high-ticket return/leakage risk.

## Workbook Structure
- `rawdata`: 10,000+ row order dataset with formatted dates/discounts and `VLOOKUP` columns (`Warranty_Months`, `Support_Team`, `Support_Region`).
- `product rule`: Lookup reference table with **Data Validation** rules.
- **MIS Summary & Trend Views:** Category lifecycle rate table (`100%` sum check), revenue & leakage table (`Lost Revenue` and `Revenue Loss %`), monthly trend view grouped by `Order_Date` month, `Warranty_Months` slicer, Pivot Chart, and executive action notes.
-
