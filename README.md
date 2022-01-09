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

## Design a Study Comparing the MechaCar to the Competition

