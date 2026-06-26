# pranavbhoir_2511745_part3_regression_insights

## TASK 1 : UNDERSTAND THE DATASET

1. Dependent variable :  monthly_sales

2. Potential independent variables :

marketing_spend
footfall
avg_discount_pct
staff_count
inventory_availability_pct
competitor_distance_km
customer_rating
holiday_flag
region
store_type


3. Numerical variables : 

marketing_spend
footfall
avg_discount_pct
staff_count
inventory_availability_pct
competitor_distance_km
customer_rating
holiday_flag

4. Categorical variables

region
store_type
holiday_flag

5. Variables that may need cleaning or transformation

customer_rating 
competitor_distance_km
region
store_type
holiday_flag 

6. Variables that may not be useful for regression

store_id 
month  


README Requirements

1. Business problem summary

purpose of the study is for a retail chain company to determine the business elements that affect their sales per month. In other words, the company wishes to conduct regression analysis to see the relationship between sales and the following variables: marketing costs, customer traffic, inventory level, and regional location.

2. Dataset description

dataset contains monthly store-level business performance data for multiple retail stores.

key variables include:

Store ID
Region
Store Type
Marketing Spend
Footfall
Average Discount Percentage
Inventory Availability Percentage
Customer Rating
Monthly Sales (Target Variable)

dataset includes both numerical and categorical variables requiring data preparation before regression analysis.

3. Dependent and independent variables

Dependent Variable
Monthly Sales
Independent Variables
Marketing Spend
Footfall
Inventory Availability Percentage
Customer Rating
Average Discount Percentage
Region (Dummy Variables)

4. Regression approach

three regression models were developed:

simple Regression Model 1
monthly Sales vs. Marketing Spend
simple Regression Model 2
monthly Sales vs. Footfall
multiple Regression Model
monthly Sales vs. Marketing Spend, Footfall, Inventory Availability Percentage, and Region Dummy Variables

models were evaluated using:

regression coefficients
R-squared values
p-values
residual analysis
business interpretation

5. Dummy variable approach

categorical variable Region was converted into dummy variables.

created dummy variables:

North
South
West

east region was selected as the reference category and excluded from the regression model to avoid the dummy variable trap.

6. Model comparison summary


 model                                 R  square    summary                                                   

 simple Regression (Marketing Spend)     0.167     limited explanatory power.                                
 simple Regression (Footfall)            0.736     strong relationship with monthly sales.                   
 multiple Regression                     0.811     best performing model with the highest explanatory power

7. Final model selected

Multiple Regression Model was selected because:

highest R² (0.811)
includes multiple business drivers
most variables are statistically significant
provides better predictive performance than the simple regression models


8. Business recommendation

according to the regression analysis, leadership should concentrate on:

lncreasing customer traffic using effective marketing and customer engagement.
ensuring sufficient inventory to avoid losses.
marketing expenditure optimization to improve sales efficiency.
learning from well-performing zones like South and West.
applying the regression analysis as a decision-making support tool by incorporating the results with business knowledge.

9. Assumptions and limitations

assumptions

there is linearity between the variables.
variables are measured without errors.
residuals are independent.
regression assumptions are mostly met.

limitations

correlation does not imply causation.
extraneous factors like competition, seasonality, price, and economic factors were not considered.
some stores have high residual values, which means other factors are affecting the store sales.
North region variable is not significant and should be used with caution.


10. Screenshots included

simple_regression_output.png
multiple_regression_output.png
residuals_preview.png
model_comparison_preview.png
