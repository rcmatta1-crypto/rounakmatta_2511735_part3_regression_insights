# Residual Analysis

## Predicted Sales Calculation

Predicted sales were calculated using the final multiple regression model:

Predicted Sales

=

149038.03

* 1.1830 × marketing_spend

* 33.9480 × footfall

* 2804.17 × inventory_availability_pct

− 16716.89 × East_dummy

Residuals were calculated as:

Residual = Actual Sales − Predicted Sales

---

## Largest Positive Residuals

The five records with the largest positive residuals correspond to stores where actual sales exceeded predicted sales.

These observations indicate that the model underestimated store performance.

Possible explanations include:

* Strong local demand.
* Effective store management.
* Promotional activities not captured in the dataset.
* Seasonal effects not included in the model.

---

## Largest Negative Residuals

The five records with the largest negative residuals correspond to stores where actual sales were below predicted sales.

These observations indicate that the model overestimated store performance.

Possible explanations include:

* Temporary stock shortages.
* Operational issues.
* Local competition.
* Unobserved economic factors.

---

## Business Interpretation

Large positive residuals suggest stores performing better than expected.

Large negative residuals suggest stores underperforming relative to expectations.

These stores may require further investigation to identify hidden drivers of performance.

---

## Under-Prediction and Over-Prediction

The model may under-predict stores that benefit from favorable local conditions or strong management.

The model may over-predict stores facing operational challenges or local competitive pressures.

Because the model does not include seasonality, customer demographics, pricing strategy, or competitor activity, some prediction errors are expected.

Overall, the model explains approximately 81% of the variation in monthly sales and provides useful business insights despite these limitations.



