# Business Data Cleaning, Validation & Excel Reporting

## Problem Summary

This project focuses on cleaning, validating, and preparing a retail sales dataset for business analysis. The raw dataset contained inconsistent text formatting, missing values, duplicate records, invalid discounts, incorrect shipping dates, and business rule violations. The objective was to transform the raw data into a clean, analysis-ready dataset and generate business reports using Microsoft Excel.

---

## Dataset Description

The dataset contains retail order-level information including:

* Order ID
* Customer Name
* Segment
* Region
* State
* City
* Category
* Sub Category
* Order Date
* Ship Date
* Ship Mode
* Quantity
* Unit Price
* Discount
* Cost
* Sales
* Profit
* Payment Status
* Order Status

---

## Tools Used

* Microsoft Excel
* Pivot Tables
* Excel Functions (TRIM, IF, IFERROR, COUNTIF, ROUND, YEAR, MONTH, TEXT)
* GitHub
* VS Code

---

## Data Cleaning Steps Performed

The following cleaning operations were performed:

* Removed extra spaces from text fields.
* Standardized text formatting.
* Corrected inconsistent category names.
* Standardized order and ship dates.
* Filled missing Region values with **Unknown**.
* Filled missing Ship Mode values with **Unknown**.
* Replaced missing Discount values with **0** where applicable.
* Identified and removed exact duplicate records.
* Flagged duplicate Order IDs for manual review.
* Created calculated columns:

  * Cleaned Discount
  * Calculated Sales
  * Calculated Profit
  * Profit Margin
  * Shipping Delay Days
  * Order Month
  * Order Year
  * Data Quality Flag

---

## Business Rules Applied

* Missing Region → Filled with Unknown
* Missing Ship Mode → Filled with Unknown
* Missing Discount → Treated as 0 when valid
* Negative Discount → Flagged as Invalid
* Discount above business limit → Flagged as Invalid
* Ship Date earlier than Order Date → Flagged as Invalid Shipping
* Cancelled Orders excluded from completed sales analysis
* Failed Payments excluded from completed sales analysis
* Refunded Orders summarized separately

---

## Data Quality Issues Found

* Missing Region values
* Missing Ship Mode values
* Missing Discount values
* Exact Duplicate Records
* Duplicate Order IDs
* Invalid Discount values
* Invalid Shipping Dates
* Sales and Profit calculation mismatches

---

## Pivot Reports Created

* Sales and Profit by Region
* Sales and Profit by Category and Sub Category
* Order Count by Ship Mode
* Profit Margin by Customer Segment
* Refunded, Cancelled and Failed Orders by Region
* Monthly Sales Trend

---

## Key Business Insights

* Sales performance varies significantly across different regions.
* Technology and Office Supplies contribute a major share of revenue.
* Standard Class is the most frequently used shipping mode.
* Invalid shipping records require further business review.
* Duplicate records and invalid discounts were successfully identified and flagged.

---

## Assumptions

* Missing Region values were replaced with "Unknown".
* Missing Ship Mode values were replaced with "Unknown".
* Missing Discount values were treated as 0 only when other sales fields were valid.
* Business rules were applied according to the assignment instructions.

---

## Limitations

* Flagged records require manual verification.
* Business decisions were not modified beyond the given rules.
* Original raw dataset was preserved without any changes.

---

## Repository Structure

```text
part1_data_cleaning/
├── data/
│   ├── raw_orders.xlsx
│   └── cleaned_orders.xlsx
├── outputs/
│   ├── data_quality_report.xlsx
│   ├── pivot_summary.xlsx
│   └── cleaning_log.md
├── screenshots/
│   ├── raw_data_preview.png
│   ├── cleaned_data_preview.png
│   ├── pivot_summary_1.png
│   └── pivot_summary_2.png
└── README.md
```

---

## Screenshots Included

* Raw Dataset Preview
* Cleaned Dataset Preview
* Pivot Summary 1
* Pivot Summary 2

---

## Conclusion

The raw retail dataset was successfully cleaned, validated, and transformed into an analysis-ready dataset. All required business rules were implemented, data quality issues were documented, and business summary reports were generated using Microsoft Excel.
