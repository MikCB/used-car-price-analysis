# What Drives the Price of a Used Car?

## Project overview

This project analyzes a used-car listings dataset to identify which vehicle attributes are most associated with price. The business audience is a used-car dealership that wants better guidance for inventory and pricing decisions.

The analysis follows the CRISP-DM process: business understanding, data understanding, data preparation, modeling, evaluation, and deployment recommendations.

## What is in this repo

The main completed notebook is `used_car_price_analysis.ipynb`. It includes the data cleaning, exploratory analysis, modeling, visualizations, evaluation, and recommendations.

The file `analysis_summary.json` stores the key model and data summary outputs from the notebook.

The file `used_car_price_assignment_upload.zip` contains the full packaged assignment, including the original course data and starter image assets.

## Data summary

The raw dataset has 426,880 rows and 18 columns. After cleaning and filtering unrealistic prices and incomplete modeling fields, the modeling dataset has 333,327 rows.

The target variable is `price`. Important predictors include year, odometer, manufacturer, condition, fuel, title status, transmission, drive, vehicle type, paint color, state, and region.

## Modeling results

The notebook compares a median-price baseline, linear regression, Ridge regression, and Lasso regression using cross-validation. The best model in this run was Ridge regression with alpha 10.0.

The best model had an average log-price RMSE of 0.402 and an average dollar MAE of about $4,840.

## Key findings

Car age and odometer reading were the strongest predictors. Newer cars and lower-mileage cars tended to have much higher predicted prices.

Vehicle configuration also mattered. Four-cylinder vehicles, front-wheel-drive vehicles, and some fuel categories tended to predict lower prices after accounting for the other variables in the model.

Vehicle type mattered as well. Pickups and trucks tended to hold stronger prices than many smaller vehicle types.

The results should be interpreted as predictive associations, not causal estimates.

## Recommendations

Prioritize newer and lower-mileage vehicles when acquiring inventory.

Treat title status as a major value signal. Clean-title vehicles are safer inventory than salvage, rebuilt, missing, lien, or parts-only titles.

Use vehicle type and manufacturer mix to guide stocking decisions, especially when comparing trucks, pickups, SUVs, sedans, and economy vehicles.

Improve listing completeness for fields such as condition, drive, size, and vehicle type, since missing values weaken pricing confidence.

Use the model as a pricing support tool rather than an automatic pricing decision.

## Next steps

Future versions of this analysis would benefit from local dealership transaction data, days on lot, reconditioning cost, and current local comparable listings.
