## TASK 3 : CREATE DUMMY VARIABLE

1. categorical variable used

variable region was converted into dummy variable for use in regression model cause regression analysis required numerical values

dataset contains four region categories:

East
North
South
West

2. Reference Category

East selected as a reference category

in order to prevent Dummy Variable Trap (perfect multicollinearity), one of the variables is left out of the model. As such, East was dropped as the benchmark.

3. dummy variable created
dummy variable is created in regression\_workbook.xlxsx file in dummy variable sheet

following Excel formulas were used:



North:



=IF(region="North",1,0)



South:



=IF(region="South",1,0)



West:



=IF(region="West",1,0)



4. interpretation

coefficients of the dummy variables show the expected difference in monthly sales compared with East stores while holding all other variables constant.

For example:

North coefficient = 10,547.38
South coefficient = 21,940.49
West coefficient = 17,491.37

This means that on average South stores are associated with approximately ₹21,940 higher monthly sales than East stores after controlling for marketing spend, footfall, and inventory availability.



## TASK 4 : RUN SIMPLE REGRESSION MODEL

1. Footfall and Monthly Sales

sales per month were used as dependent variable in regression analysis against footfall. The regression resulted in an R-square value of 0.736, which implies that footfall accounts for about 73.6 percent of variation in monthly sales. The coefficient was positive and significant. It implies that sales are high in areas with many customers.

2. Marketing Spend and Monthly Sales

regression analysis of sales against marketing expenditure was carried out. An R-square of 0.167 was obtained meaning that marketing expenditure accounts for about 16.7% of the variance in sales per month. There was a positive relationship between marketing expenditure and sales, as indicated by the regression coefficient while the probability level was less than 0.05

3. Comparison

footfall model clearly had superior predictive power over the marketing spend model. It follows that footfall is likely a better predictor of monthly sales than marketing spend when considered separately.



## TASK 5 : RUN MULTIPLE REGRESSION MODEL

1. Intercept

Intercept                    131460.3072

2. Coefficients

marketing spend              1.18591413
footfall                     33.87042078
inventory availability pct   2818.206779
north                        10547.37963
south                        21940.48828
west                         17491.37157

3. R SQUAR = 0.811395878
4. P-values

Intercept :  0.002707148
marketing spend : 2.16628E-17
footfall : 5.4208E-101
inventory availability pct : 9.51381E-09
north : 0.148360132
south : 0.00320863
west  : 0.008029495

5. Direction of relationship

Variable                     Direction

marketing spend              Positive
footfall                     Positive
inventory availability pct   Positive
north                        Positive
south                        Positive
west                         Positive

6. Business meaning of each important variable

footfall is strongest drivers of sales.
inventory availability has large positive effect suggesting stock availability is critical.
marketing spend contributes positively to sales growth.
regional differences indicate some regions outperform the East region.

7. Any variables that appear statistically weak or difficult to interpret

North region looks statistically weak because its p-value (0.1484) is grater than threshold value (0.05) This means that the sales in North region stores are not statistically different from those in the East region it would be reasonable to interpret the North coefficient with caution. The rest of the variables look statistically significant.



## TASK 8 : WRITE MODEL EQUATION

1. Simple regression equations

model 1 : marketing spend

equation : Monthly Sales = 560777.35 + 2.13 × Marketing Spend

model 2 : Monthly Sales = 446410.58 + 35.68 × Footfall

2. Multiple Regression Equation

Monthly Sales =
131460.31

* 1.19 × Marketing Spend
* 33.87 × Footfall
* 2818.21 × Inventory Availability
* 10547.38 × North
* 21940.49 × South
* 17491.37 × West



3. Explanation of Each Coefficient



|variable|coefficient|business interpretation|
|-|-|-|
|intercept|131460.3072|estimated monthly sales when all predictors are zero and the store belongs to the reference region (East)|
|marketing Spend|1.18591413|for each extra ₹1 spent on marketing, the monthly sales go up by about ₹1.19, keeping all else constant|
|footfall|33.87042078|For each additional customer visit, there is an increase in sales of about ₹33.87.|
|inventory Availability|2818.206778|each percentage point increase in inventory availability results in an approximate sales increase of ₹2,818 per month.|
|north|10547.37963|north stores are predicted to experience ₹10,547 more monthly sales compared to East stores, all else being equal.|
|south|21940.48828|sales for South stores are expected to be approximately ₹21,940 more per month than those of East stores.|
|west|17491.37157|sales for West stores are expected to be approximately ₹17,491 more per month than those of East stores.|





4\. Explanation of Dummy Variables



categorical variable converted into dummy variable cause regression analysis requires numerical value



following are dummy variable



north

south

west



value of 1  indicates  that store belongs to that religion while 0 indicates that it does not



5\. Reference Category Used



east region used as the reference category

&#x20;

The inclusion of East would have resulted in perfect multicollinearity in the regression analysis. Consequently, the coefficients for North, South, and West can be interpreted as the differences in monthly sales in relation to the East outlets.



6\. Final Model Selected



multiple regression model is selected as the final model



7\. Reason for Selecting the Final Model



It is the model with the maximum R square 0.811395878, indicating that the variation in monthly sales can be explained by about 81.1% using this model.

It considers many drivers of business performance, such as expenditure on marketing, customer visits, inventory level, and regional variations.

Most predictor variables are statistically significant. Dummy variable for the North region is not statistically significant (p-value = 1.448923147) and needs careful interpretation.

The multiple regression model gives better insights compared to the other two models.

