# Store Sales Regression Analysis

# Business Problem Summary

The leadership team of the retail chain wants to understand which factors are most strongly associated with monthly sales performance across stores. The goal is to identify actionable drivers of sales that can support decisions related to marketing investments, inventory management, staffing, and regional prioritization.

Regression analysis was performed to quantify the relationships between business variables and monthly sales and to provide evidence-based recommendations.

---

# Dataset Description

The dataset contains store-level information and monthly performance metrics.

Variables available include:

* store_id
* month
* region
* store_type
* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* monthly_sales
* monthly_profit

The dataset contains both numerical and categorical variables.

---

# Dependent and Independent Variables

## Dependent Variable

monthly_sales

This variable represents store sales performance and is the target variable used in regression analysis.

## Independent Variables

The following variables were considered as predictors:

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* customer_rating
* region
* store_type
* holiday_flag

---

# Regression Approach

Three models were developed.

### Model 1

Simple Regression:

monthly_sales vs marketing_spend

R² = 0.1672

---

### Model 2

Simple Regression:

monthly_sales vs footfall

R² = 0.7363

---

### Model 3

Multiple Regression:

Dependent Variable:

monthly_sales

Independent Variables:

* marketing_spend
* footfall
* inventory_availability_pct
* East_dummy

R² = 0.8102

Adjusted R² = 0.8078

The multiple regression model demonstrated the strongest explanatory power.

---

# Dummy Variable Approach

Categorical variables cannot be directly used in regression analysis. Therefore dummy variables were created.

Region categories:

* East
* North
* South
* West

The West region was selected as the reference category.

Dummy variables were created for East, North and South, while West was excluded to avoid multicollinearity and the dummy variable trap.

In the final model, East_dummy was included.

East_dummy = 1 for East stores.

East_dummy = 0 otherwise.

---

# Model Comparison Summary

| Model                               | Variables                                                         | R²     |
| ----------------------------------- | ----------------------------------------------------------------- | ------ |
| Simple Regression – Marketing Spend | marketing_spend                                                   | 0.1672 |
| Simple Regression – Footfall        | footfall                                                          | 0.7363 |
| Multiple Regression                 | marketing_spend, footfall, inventory_availability_pct, East_dummy | 0.8102 |

The multiple regression model performed best and explained approximately 81% of the variation in monthly sales.

---

# Final Model Selected

The multiple regression model was selected as the final model.

Variables included:

* marketing_spend
* footfall
* inventory_availability_pct
* East_dummy

Reasons for selecting the model:

* Highest R² value.
* All variables were statistically significant.
* Multiple business drivers were captured simultaneously.
* Strong practical usefulness for management decisions.

---

# Business Recommendation

The analysis suggests that customer footfall is the strongest factor associated with monthly sales.

Leadership should focus on:

* Increasing customer traffic.
* Maintaining inventory availability.
* Investing in marketing activities.
* Investigating the weaker performance of East region stores.

The multiple regression model should be used as the primary decision-support model.

---

# Assumptions and Limitations

## Assumptions

* Linear relationships exist between predictors and sales.
* Observations are independent.
* Data accurately reflects store performance.
* Dummy variables adequately represent categorical information.

## Limitations

The model does not capture:

* Seasonality effects.
* Economic conditions.
* Competitive actions.
* Customer demographics.
* Pricing strategies.
* Promotional campaigns.
* Store management quality.

Regression identifies association and not definitive causation.

---

# Screenshots Included

The repository includes the following screenshots:

1. screenshots/simple_regression_output.png

Contains regression statistics and coefficient tables for simple regression.

2. screenshots/multiple_regression_output.png

Contains the multiple regression output.

3. screenshots/model_comparison_preview.png

Contains comparison of all models.

4. screenshots/residuals_preview.png

Contains predicted sales and residual analysis.

---

# Conclusion

The multiple regression model explains approximately 81% of the variation in monthly sales and provides strong evidence that customer footfall, inventory availability, and marketing expenditure are important drivers of sales performance. These insights can help leadership allocate resources and improve store performance while recognizing that regression measures association rather than causation.
