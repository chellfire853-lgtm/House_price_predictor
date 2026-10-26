# California House Price Predictor

Predicts median house value for California census districts from location, income, and housing features.

## Approach
- **Data:** 20,640 districts (1990 California census), 9 features + target `median_house_value`.
- **Cleaning:** median imputation for 207 missing `total_bedrooms`; one-hot encoding for `ocean_proximity`; scaling for numeric features.
- **Feature engineering:** rooms per household, bedrooms per room, people per household.
- **Models:** Linear Regression (baseline) vs Random Forest (200 trees), 80/20 train/test split.



Random Forest cuts the error by about 36% vs. the baseline. Median income is by far the strongest predictor .

## Limitations / next steps
- Target is capped at $500k, which hurts accuracy on expensive districts.
- Try gradient boosting (XGBoost/LightGBM), hyperparameter tuning with cross-validation, and a map-based visualization.
