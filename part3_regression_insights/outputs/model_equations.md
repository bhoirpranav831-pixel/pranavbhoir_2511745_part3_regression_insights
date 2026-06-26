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
dummy variable is created in regression_workbook.xlxsx file in dummy variable sheet 

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
