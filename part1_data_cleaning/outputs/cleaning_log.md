# Data Cleaning Log

## Project Overview

This document records all data cleaning, validation, and business rule implementation steps performed on the retail orders dataset.

---

## Issues Found

The following issues were identified in the raw dataset:

* Extra spaces in text fields
* Inconsistent capitalization in customer names, categories, and regions
* Missing values in Region
* Missing values in Ship Mode
* Missing values in Discount
* Duplicate rows
* Duplicate Order IDs with conflicting information
* Invalid discount values (negative and above allowed limit)
* Ship dates earlier than order dates
* Sales and profit calculation mismatches

---

## Cleaning Actions Performed

The following cleaning operations were applied:

* Removed leading and trailing spaces using TRIM.
* Standardized text formatting using PROPER, UPPER, Find & Replace, and Flash Fill where required.
* Standardized category and sub-category names.
* Converted Order Date and Ship Date into a consistent date format.
* Filled missing Region values with **Unknown**.
* Filled missing Ship Mode values with **Unknown**.
* Replaced missing Discount values with **0** only where other sales information was valid.
* Flagged negative discounts as Invalid.
* Flagged discounts above the allowed business limit as Invalid.
* Identified and removed exact duplicate records.
* Flagged duplicate Order IDs for manual review.
* Calculated shipping delay in days.
* Created calculated sales, calculated profit, profit margin, order month, and order year columns.
* Added data quality flags for each record.

---

## Business Rules Applied

The following business rules were implemented:

* Missing Region → Filled with **Unknown**
* Missing Ship Mode → Filled with **Unknown**
* Missing Discount → Replaced with **0** (where applicable)
* Negative Discount → Flagged as Invalid
* Discount above business limit → Flagged as Invalid
* Ship Date earlier than Order Date → Flagged as Invalid Shipping
* Cancelled Orders → Excluded from completed sales analysis
* Failed Payments → Excluded from completed sales analysis
* Refunded Orders → Reported separately in pivot summary

---

## Records Removed

* Exact duplicate records were removed from the cleaned dataset.

---

## Records Flagged

The following records were flagged for review:

* Duplicate Order IDs
* Invalid discounts
* Invalid shipping records
* Warning records due to missing Region or Ship Mode

---

## Assumptions

* Missing Region values were replaced with "Unknown".
* Missing Ship Mode values were replaced with "Unknown".
* Missing Discount values were treated as 0 where valid.
* Original raw dataset was preserved without modification.

---

## Limitations

* Business rules were applied only according to the assignment requirements.
* Records with conflicting business information were flagged instead of automatically corrected.
* Final business decisions for flagged records require manual review.

---

## Output Files Generated

* cleaned_orders.xlsx
* data_quality_report.xlsx
* pivot_summary.xlsx
* cleaning_log.md

---

## Conclusion

The dataset has been cleaned, validated, and transformed into an analysis-ready format. All required business rules were applied, calculated columns were created, data quality issues were documented, and summary reports were prepared for business analysis.
