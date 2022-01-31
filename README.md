## Overview of Project
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

# Deliverable 1:  
## Linear Regression to Predict MPG
### Deliverable Requirements:
**Resulting Model:** 
				
Statistical Summary:
![d1](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/linear_regression_d1.png)

From the above output we can see that:
1. The p-Value for this model,p-Value: 5.35e-11, is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further indcates that the slope of this linear model is not zero.

2.  This linear model has an r-squared value of 0.7149, which means that approximately 71% of all mpg predictions will be determined by this model. Relatively speaking, his multiple regression model does predict mpg of MechaCar prototypes effectively. 

If we remove the less impactful independent variables (vehicle weight, spoiler angle, and All Wheel Drive), the predictability does decrease, but not drastically: the r-squared value falls from 0.7149 to 0.674. 

![d1](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/new_linear_regression_d1.png)


# Deliverable 2:  
### Deliverable Requirements:

Your `total_summary` dataframe should look like this:

![d1](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/D2.4.png)

Write an RScript that creates a `lot_summary` dataframe using the `group_by()` and the `summarize()` functions to group each manufacturing lot by the mean, median, variance, and standard deviation of the suspension coil’s PSI column.
Your lot_summary dataframe should look like this:

![d1](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/D2.3.png)

# Deliverable 3:  
### Deliverable Requirements:

The next step is to conduct a t-test on the suspension coil data to determine whether there is a statistical difference between the mean of this provided sample dataset and a hypothesized, potential population dataset. Using the presumed population mean of 1500, we find the following:

There is a summary of the t-test results across all manufacturing lots
![d3](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/t_test_all.png)

From here we can see the true mean of the sample is 1498.78, which we also saw in the summary statistics above.  With a p-Value of 0.06, which is higher than the common significance level of 0.05, there is NOT enough evidence to support rejecting the null hypothesis.  That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500. 

Next looking at each individual lots:

1. Lot 1 sample actually has the true sample mean of 1500, again as we saw in the summary statistics above. With a p-Value of 1, clearly we cannot reject (i.e. accept) the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean (1500).
2. Lot 2 has essentially the same outcome with a sample mean of 1500.02, a p-Value of 0.61; the null hypothesis cannot be rejected, and the sample mean and the population mean of 1500 are statistically similar.
3. However, Lot 3, not surprisingly is a different scenario. Here the sample mean is 1496.14 and the p-Value is 0.04, which is lower than the common significance level of 0.05.  All indicating to reject the null hypothesis that this sample mean and the presumed population mean are not statistically different.

 ![d3](https://github.com/Anuradha0/MechaCarChallenge/blob/main/Resources/t_test_lot.png)

# Deliverable 4:  
### Deliverable Requirements:

Using your knowledge of R, design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.

The statistical study design has the following:
- A metric to be tested is mentioned
- A null hypothesis or an alternative hypothesis is described
- A statistical test is described to test the hypothesis

This study would involve collecting data on MechaCar and its comparable models across several different manufacturers over the last 3 years.
* What are the competitions' comparable models, 
* Which cars will MechaCar be competing with head-to-head? which cars will be included in the study?
* Which factors will look at the study to determine the relevant to selling price?
 
#### Metrics
Collecting data for comparable models across all major manufacturers for past 3 years for the following metrics:

*  Safety Feature Rating
*  Current Price (Selling)
*  Drive Package
*  Engine (Electric, Hybrid, Gasoline / Conventional)
*  Resale Value
*  Average Annual Cost of ownership
*  MPG

#### Hypothesis: Null and Alternative
After determining which factors are key for the MechaCar's genre:

 * Null Hypothesis (Ho): MechaCar is priced correctly based on its performance of key factors for its genre.
 * Alternative Hypothesis (Ha): MechaCar is NOT priced correctly based on performance of key factors for its genre.
 
#### Statistical Tests
A multiple linear regression would be used to determine the factors that have the highest correlation/predictability with the list selling price (dependent variable); which combination has the greatest impact on price (it may be all of them!)
