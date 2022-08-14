# MechaCar Statistical Analysis

## Overview

In this project, statistical tests and analysis were performed using R. A company,  AutosRUs, wants to utilize data analytics in all their decision making as they believe that will make them have very successful automobile launches. 

As the primary analyst for the data analytics team of the company, I am responsible for  performing  retrospective analysis of historical data, analytical verification and validation of current automotive specifications and study design of future product testing.
 
I have to ensure that analysis I perform contains a statistical backbone, a quantitative metric and clear interpretation of the results. Summary statistics will also be provided for different variables, visualizations for different datasets and interpretation of statistical test results. Also, using my critical thinking skills, I will propose my own study design,  hypotheses and analysis workflow that will make autosRUs manufacturing processes even better. 

In my first ever project I will be working on AutosRUs’ newest prototype, the MechaCar. It is suffering from production troubles that are blocking the manufacturing team’s progress. My task here is to review the production data for insights that may help the manufacturing team. I will be performing these specific tasks:
1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population
4. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, I'll write a summary interpretation of the findings.

## Linear Regression to Predict MPG
Below are the summary results from the linear regression:

![image1](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/deliverable1_results.png)

In performing this analysis, I aimed to answer some three specific questions. The questions and the answers  to them after my analysis are gien below:

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle length, and vehicle ground clearance provided a non-random amount of variance to the mpg values in the dataset. These variables had very small p-values which implies they have a high level of significance on miles per gallon on the MechaCar prototype. On the other hand, the vehicle weight, spoiler angle, and All Wheel Drive (AWD) have p-Values that indicate a random amount of variance. 


2. Is the slope of the linear model considered to be zero? Why or why not?
The slope of the linear model is not zero. This is because, the p-Value of 5.35e-11 is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis, which further implies that the slope of the linear model is not zero.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
The R-squared value is what indicates whether the linear model predicts the mpg of the MechaCar. For this linear model, the R-squared value was 0.7149 which means 71.5% of all mpg predictions will be determined corectly by the model. Thus, the linear model can be considered effective.

## Summary Statistics on Suspension Coils

![image2](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.png)

![image3](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.png)

# Question
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

When looking at all the manufacturing lots in total, the variance of the coils is 62.29356 PSI, which is within the 100 PSI variance requirement.
However, when we are considering each lot individually, Lot 1 and Lot 2 are within the design specifications with variances of 0.9795918 and 7.4693878 respectively. Lot 3 on the other hand has a very high variance of 170.2861224 which exceeds the manufacturing specifications.  Therefore, Lot 3 on its own does not meet the design specifications. 

## T-Tests on Suspension Coils
### T-Test across all lots 
Below is the summary of the t-test results across all lots:

![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/All_Lots.png)

The results above show that the mean of the sample is 1498.78 With a p-Value of 0.06, which is higher than the significance level of 0.05. Therefore, there isn't enough evidence to support rejecting the null hypothesis. That is to say, the mean of all three of these manufacturing lots is statistically similar to the presumed population mean of 1500.

### T-Test across Lot 1
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot1.png)

Lot 1 had a mean of exactly 1500 with a p-Value of 1. Therefore, we cannot reject the null hypothesis that             there is no statistical difference between the observed sample mean and the presumed population mean (1500).

### T-Test across Lot 2
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot2.png)

Lot 2 has a similar outcome with a sample mean of 1500.02 and a p-Value of 0.61. Thus the null hypothesis cannot be rejected,                and the sample mean and the population mean of 1500 are statistically similar.

### T-Test across Lot 3 
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot3.png)

For Lot 3 the sample mean is 1496.14 and the p-Value is 0.042 which is lower than the significance level of 0.05. Therefore, we can reject the null hypothesis that                 this sample mean and the presumed population mean are not statistically different.


## Study Design: MechaCar vs Competition
Next, I would want to design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers.
For this analysis , the metrics I want to test are highway fuel efficiency and horse power as these are metrics that are of high interest to consumers.
The Null Hypothesis is that all of the cars in the same class have the same fuel efficienies. The Alternative Hypothesis is that they are not all the same.

I would use ANOVA test to complete this analysis for both types of fuel efficiencies and horse power . I would use the ggplot2 library to show the spread between different cars using a boxplot.

I would need highway fuel efficiency and horsepower data from 50 individual cars to create a sample size of data for each car in the class type. So if there are 10 cars in each class type, I would have 500 data points collected for each fuel efficiency and horsepower.

What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why?
What data is needed to run the statistical test?
