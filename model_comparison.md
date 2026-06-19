# Model Comparison

## Model 1: Simple Regression – Marketing Spend

### Variables Used

Dependent Variable:

monthly_sales

Independent Variable:

marketing_spend

### R-Squared

R² = 0.1672

This model explains approximately 16.7% of the variation in monthly sales.

### Significant Variables

marketing_spend

P-value = 2.48 × 10^-14

### Business Usefulness

Marketing spending positively affects sales and provides useful information regarding advertising decisions.

### Limitations

The model ignores other important factors such as customer traffic and inventory availability.

---

## Model 2: Simple Regression – Footfall

### Variables Used

Dependent Variable:

monthly_sales

Independent Variable:

footfall

### R-Squared

R² = 0.7363

This model explains approximately 73.6% of the variation in monthly sales.

### Significant Variables

footfall

P-value = 4.75 × 10^-94

### Business Usefulness

Footfall is a strong driver of sales and helps management understand the importance of customer traffic.

### Limitations

The model ignores marketing activity and inventory factors.

---

## Model 3: Multiple Regression

### Variables Used

Dependent Variable:

monthly_sales

Independent Variables:

* marketing_spend
* footfall
* inventory_availability_pct
* East_dummy

### R-Squared

R² = 0.8102

Adjusted R² = 0.8078

The model explains approximately 81% of the variation in monthly sales.

### Significant Variables

marketing_spend

P-value = 2.4 × 10^-17

footfall

P-value = 1 × 10^-101

inventory_availability_pct

P-value = 1.1 × 10^-8

East_dummy

P-value = 0.00245

All variables are statistically significant.

### Business Usefulness

The multiple regression model provides the strongest explanatory power and helps management understand how multiple factors jointly influence sales performance.

The model suggests that increasing footfall, improving inventory availability, and investing in marketing can improve monthly sales.

### Limitations

The model does not capture:

* Seasonal effects
* Competitor behavior
* Economic conditions
* Customer demographics
* Pricing strategies

---

# Overall Comparison

Among the three models, the multiple regression model performs best because it explains the highest proportion of variation in monthly sales.

Although simple regression models provide useful insights individually, the multiple regression model offers superior decision-making support by incorporating multiple drivers simultaneously.
