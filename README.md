# MechaCar_Statistical_Analysis
The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle.

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.

## Linear Regression to Predict MPG
In the first part of this analysis, five columns (vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance) in the MechaCar_mpg.csv dataset are used to predict MPG using Multiple Linear Regression in R. 
Then, by using the Summary() function and determining the p-value for each parameter, we decide which variables/coefficients provided a non-random variance to the mpg values in the dataset?

![This is an image](/D1.jpg)

As we see in the above picture, the P-value for vehicle_length and ground_clearance is less than 0.05, which means they correlate with our target variable, MPG. On the other hand, P-value for spoiler_angle, AWD (drive_train), and vehicle_weight is more than 0.05, so we could assume that they don't correlate to MPG values, and they change randomly.
In addition, the p-value of our linear regression analysis is 5.35 x e-11, which is much smaller than our assumed significance level of 0.05%. Therefore, we can state that there is sufficient evidence to reject our null hypothesis, which means that the slope of our linear model is not zero.
Also Multiple R-squared is 0.7149 which means MPG values could explain/predict 71.49% by our Linear Regression Model.


## Summary Statistics on Suspension Coils
In the second part, from Suspension_Coil.csv, an RScript is written that creates a total_summary data frame using the summarize() function to get the mean, median, variance, and standard deviation of the suspension coil's PSI column.

![This is an image](/D21.jpg)

Then by grouping by each Manufacturing lot, the mean, median, variance, and standard deviation are calculated separately for each lot. 

![This is an image](/D22.jpg)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.
As we can see in results, The variance for Lot1 and Lot2 is less than 100 pounds per square inch and pass the standard, However for Lot3 it exceeds acceptable range and it's not meet our standard criteria.


## T-Tests on Suspension Coils
In this part, t-tests perform to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. First t.test() function used to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

![This is an image](/D31.jpg)

Assuming our significance level was the common 0.05 percent, our p-value is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the two means are statistically similar.

Next, three more t.test() function are used to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

![This is an image](/D32.jpg)

For Lot1 and Lot2, our p-value is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the two means are statistically similar.
However, for Lot3,  our p-value is less than our significance level. S, we have sufficient evidence to reject the null hypothesis, and we would state that the two means are not statistically similar.


