# Challenge15- MechaCar Statistical Analysis

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. Data Analytics team is reviewed production data for insights that may ghelp manufacturing team. 

## Linear Regression to Predict MPG

We want to predict the MPG, to do so, we executed a Multiple Linear Regression (MLR) using MechaCar_mpg.csv basis containing historical information of the MPG per vehicle associated with its length, weight, spoiler's angle, ground clearance, and AWD. 

The model assumes a linear relation as follows: 

mpg ~ a1 * vehicle_length + a2 * vehicle_weight + a3 * spoiler_angle + a4 * ground_clearance + a5 * AWD + C

The analysis results are as follows: 

**Multiple Linear Regression Model Results**


![MLR](MLR.png)

The MLR explains over 70% of the total variance which is strong enough to consider its results as indicative, additionally, in the summary output, the last column show the probability that each coefficient contributes a random amount of variance to the linear model, thus, vehicle length and ground clearance seems to de determinant in the vehicle's MLR (intercept is statistically significant too, but probably is just working as a fit among scales). 

Both statistically significant variables have non-zero coeficients and both are positive, this means that increases in any of them may result in an increase in the MPG of the vehicle. 

## Summary Statistics on Suspension Coils

Four our second analysis ,we receved the Suspension_Coil.csv dataset, this one contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots, the design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. 

**Total Summary**


![Total_Summary](Total_Summary.png)

**Summary per Lot**


![LOT_Summary](LOT_Summary.png)

We can conclude two things: 

1) Variance of the suspensions comply with design specifications at a Total level. 
2) Lot 3's is inconsistent since its variance exceeds the maximum pounds per square inch agreed.


## T-Test on Suspension Coils

General PSI of the total production has a 1,500 pounds per square inch mean, we now want to know if the new lots are in line with the total population (production) of the plant. To do so, we are testint through a T Test on the total lots and per lot:  

**T Test of the total production**


![t_test_total](t_test_total.png)

**T- Test per Lot**


![t_test_1](t_test_1.png)
![t_test_2](t_test_2.png)
![t_test_3](t_test_3.png)

Recall: Assuming our significance level was the common 0.05 percent, if our p-value is above our significance level we do not have sufficient evidence to reject the null hypothesis, and we would state that the the tasted mean is statistically similar to the population's mean. 

Results: 

1) Total Production's mean is statistically similar to the population's mean. 
2) Lot 1 (Mean = 1,500) and Lot 2 (Mean=1,500.2) are also statistically similar to the population's mean, lot 3 (Mean = 1,496.14) is not. 


## Design a Study Comparing the MechaCar to the Competition

As some final comments on the study, we would like to propose some further analysis that may be performed to test MechaCar performance against our competition at consumer's preference.

### Consumer's Prefer Specs ###

We may want to review our competitor's total sales against each model specs to identify which are the specs that customers evaluate as more important in the top sales models, to do so, we would need to get statistical information of the sales per model and the main specs to run a regression as follows: 

**total_sales = a1 * Spec_1 + a2 * Spec_2 + ... + an * Spec_n + C**

Results still need to be reviewed to identify statistically significance per Spec (p value) and total regression explanation power (R^2), if data is adequate, this analysis would let us identify if our models are competitive at specs level vs competition's top sellers. 

Note specs range from MPG to specific media or security techonologies. 

### AB Test ###

### Price Elasticity ###

Another easy analysis that may be useful would be to measure the direct price elasticity through a linear model of sales vs prices ( multiple excercises grouped by category) to identify how changes in prices may affect demand: 

**Sales_per_group = a1* Price_of_vehicles_in_group + C**

In this exercise, C is kind of a base demand for specific groups, nevertheless, the coefficient (expected to be negative) if statistically significant would let us know how increases or decreases of price may reduce or increase demand. 

This information is pretty straightforward but allows us to see if our pricing campaigns are in line with the market and also if there is an interesting trade-off between price reduction and volume increase when the manufacturing process got inventories. 

For this exercise, we would need an exhaustive database of last year's (or as recent as possible) sales per category and updated prices in our target markets. If the data comply with linear regression assumptions, we can rely on the results of the analysis. 
