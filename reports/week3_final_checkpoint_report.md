# KisanAI AgriTech — Week 3 Checkpoint Report

## Objective
Train crop-specific yield prediction models and evaluate
their performance using RMSE and MAPE.

## Dataset Preparation
- Historical crop production records from Karnataka,
  Maharashtra and Telangana.
- 4,916 cleaned district-crop-year records.
- 4,415 records with valid previous-year yield features.
- 98 state-district combinations after cleaning.
- Historical crops: Rice, Soybean, Cotton and Sugarcane.
- Tomato evaluated separately using another dataset.

## Historical Model Features
- State
- District
- Year
- Previous-year yield

Historical models do not yet combine weather and soil type.

## Cleaned Random Forest Results

| Crop | RMSE | MAPE | Unit |
|---|---:|---:|---|
| Rice | 0.5816 | 23.04% | Tonnes/ha |
| Soybean | 0.5849 | 38.14% | Tonnes/ha |
| Cotton | 1.3449 | 41.75% | Bales/ha |
| Sugarcane | 21.3894 | 25.59% | Tonnes/ha |

## Baseline Comparison

| Crop | Random Forest RMSE | Baseline RMSE |
|---|---:|---:|
| Rice | 0.5816 | 0.5521 |
| Soybean | 0.5849 | 0.4872 |
| Cotton | 1.3449 | 1.5686 |
| Sugarcane | 21.3894 | 18.1121 |

Cotton Random Forest outperformed the previous-year
baseline by approximately 14.26% in RMSE.

## Gradient Boosting Results

| Crop | Gradient Boosting RMSE |
|---|---:|
| Rice | 0.6108 |
| Soybean | 0.5285 |
| Sugarcane | 19.6701 |

Gradient Boosting did not outperform the previous-year
baseline on the tested crops.

## Soil Feature Investigation
The AgriMind dataset includes:
- Soil pH
- Nitrogen
- Phosphorus
- Potassium

An earlier experiment tested these features for Cotton,
but the dataset lacks district-level identifiers needed
to merge them reliably with historical crop records.

Categorical soil type remains unavailable.

## Limitations
1. Historical data does not contain weather measurements.
2. Verified district-level soil-type data is unavailable.
3. Historical Tomato records are unavailable.
4. Cotton yields are in bales per hectare, while other
   historical crops use tonnes per hectare.
5. Most ML models did not outperform the baseline.
6. Historical annual yield aggregation and forecasting
   assumptions require further validation.

## Next Steps
- Obtain verified geographically matched soil data.
- Integrate historical weather data where possible.
- Improve Cotton predictions and reduce MAPE.
- Evaluate additional forecasting methods.
- Validate models on future-year holdout data.

## Conclusion
Four historical crop-specific Random Forest models were
trained and evaluated. Cotton showed improvement over
the previous-year baseline. Other crops require further
development. The combined weather, lag and categorical
soil-type modelling requirement remains incomplete.
