# KisanAI AgriTech — Week 1 EDA Report

## 1. Data Sources
Government agricultural area, production and yield reports
for Karnataka, Maharashtra and Telangana.

## 2. Data Coverage
- Original records: 1164
- Cleaned records: 1153
- States: 3
- Crop groups (4): Cereals & Millets, Foodgrains, Oilseeds and Pulses
- Agricultural years: 2020-2021 to 2022-2023

## 3. Data Cleaning
- Standardized column names and data structure.
- Converted agricultural measurements to numeric values.
- Removed 11 records with missing measurements.
- Retained valid district-level records.

## 4. Correlation Results
- Area vs Production:
  0.786
- Production vs Yield:
  0.592
- Area vs Yield:
  0.149

## 5. Key Findings
- Area and production have a strong positive association.
- Production and yield have a moderate positive association.
- Area and yield have a weak positive association.
- Telangana has the highest pooled weighted yield
  in all four crop groups in the available reports.

## 6. Limitations
- Government data currently contains crop-group aggregates rather than
  individual crop yields.
- Rainfall files have not been integrated into this analysis.
- Rice rainfall-yield correlation is not yet established.
- Cotton prediction noise has not yet been verified.
- The full client checkpoint is not complete.

## 7. Conclusion
The first stage of government agricultural data
compilation, cleaning and descriptive EDA is complete.
Rainfall integration, crop-specific analysis and the full client checkpoint
remain outstanding.
