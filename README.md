# MechaCar Statistical Analysis

## Overview

In this project, statistical tests and analysis were performed for an automobile company called AutosRUs using R. AutosRUs, wants to utilize data analytics in all their decision making as they believe that will make them have very successful automobile launches. As the primary analyst for the data analytics team of the company, I am responsible for  performing  retrospective analysis of historical data, analytical verification and validation of current automotive specifications and study design of future product testing.In my role, I ensure that analysis I perform contains a statistical backbone, a quantitative metric and clear interpretation of the results. I provide summary statistics for different variables, visualizations for different datasets and interpretation of statistical test results. Also, using my critical thinking skills, I propose my own study designs, hypotheses and analysis workflow that will make autosRUs manufacturing processes better. 

In my first ever project I will be working on AutosRUs’ newest prototype, the MechaCar. It is suffering from production troubles that are blocking the manufacturing team’s progress. I have two datsets containing information related to the miles per gallon and the suspension coils of the MechaCar. My task here is to review the production data for insights that may help the manufacturing team. I will be performing these specific tasks:
1. Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
2. Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
3. Run t-tests to determine if the manufacturing lots are statistically different from the mean population.
4. Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
For each statistical analysis, I'll write a summary interpretation of the findings.

## Linear Regression to Predict MPG
Using the miles per gallon dataset which contains mpg test results for 50 prototype MechaCars, I preformed a multiple linear regression to see if the dependent variable miles per gallon (mpg) can be predicted using the vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD) independent variables. Below is the summary results from the linear regression:

![image1](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/deliverable1_results.png)

In performing this analysis, I aimed to answer some three specific questions. The questions and the answers obtained to them after my analysis are given below:

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

The vehicle length, and vehicle ground clearance provided a non-random amount of variance to the mpg values in the dataset. These variables had very small p-values which implies they have a high level of significance on miles per gallon on the MechaCar prototype. On the other hand, the vehicle weight, spoiler angle, and AWD have p-Values that indicate a random amount of variance. 

2. Is the slope of the linear model considered to be zero? Why or why not?  

The p-Value of 5.35e-11 is much smaller than the assumed significance level of 0.05%. This indicates there is sufficient evidence to reject our null hypothesis which means the slope is not zero. Also, the linear regression showed that some of the independent variables had a significant effect on the dependent variables which further implies that the slope of the linear model is not zero.

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

The R-squared value is what indicates whether the linear model predicts the mpg of the MechaCar. For this linear model, the r-squared value was 0.7149 which means 71.5% of all mpg predictions will be determined by this model. Thus, the linear model can be considered effective.

## Summary Statistics on Suspension Coils
Using the Suspension_Coil.csv dataset which contains the results from three manufacturing lots, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. The dataset contains 150 different vehicle IDs, their lot and PSI levels. Two summary statistics tables were created to show the suspension coil’s PSI continuous variable across all manufacturing lots, and then the mean, median, variance, and standard deviation for each lot. The tables are shown below:

![image2](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.png)

![image3](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/lot_summary.png)

From the results of the analysis I seeked to answer this question:
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

When looking at all the manufacturing lots in total, the variance of the coils is 62.29356 PSI, which is within the 100 PSI variance requirement. However, when we are considering each lot individually, Lot 1 and Lot 2 are within the design specifications with variances of 0.9795918 and 7.4693878 respectively. Lot 3 on the other hand has a very high variance of 170.2861224 which exceeds the manufacturing specifications. Therefore, Lot 3 on its own does not meet the design specifications. 

## T-Tests on Suspension Coils
T-Tests were performed to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. This could be deduced using the four different p-values generated. 

### T-Test across all lots 
Below is the summary of the t-test results across all lots:

![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/All_Lots.png)

The result above shows that the mean of the sample is 1498.78 with a p-Value of 0.06, which is higher than the significance level of 0.05. Therefore, we fail to reject the null hypothesis that there is no statistical difference between the manufacturing lots' mean and the population mean of 1,500 PSI. 

### T-Test across Lot 1 
Below is the result of the t-test for lot 1:

![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot1.png)

Lot 1 had a mean of 1,500 and a p-Value of 1. Therefore, we fail to reject the null hypothesis that there is no statistical difference between the observed sample mean and the presumed population mean of 1,500 PSI.

### T-Test across Lot 2
Below is the result of the t-test for lot 2:

![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot2.png)

Lot 2 has quite a similar outcome as lot 1 with a sample mean of 1500.02 and a p-Value of 0.61. Thus the null hypothesis cannot be rejected.

### T-Test across Lot 3 
Below is the result of the t-test for lot 3:

![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot3.png)

For Lot 3 the sample mean is 1496.14 and the p-Value is 0.042 which is lower than the significance level of 0.05. Therefore, we can reject the null hypothesis that     this sample mean and the presumed population mean are not statistically different.


## Study Design: MechaCar vs Competition
Next, I would want to design a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers. For this analysis , the metrics I want to test are highway fuel efficiency and horse power as these are metrics that are of high interest to consumers. The Null Hypothesis is that all of the different classes of cars for Mechacar and its competitors have the same highway fuel efficienies and horse power. The Alternative Hypothesis is that the highway fuel efficiency and horsepower of MechaCar vehicles is higher than that of the competitors..

I would use ANOVA test to complete this analysis for both types of fuel efficiencies and horse power . I would use the ggplot2 library to show the spread between different cars using a boxplot.

I would need highway fuel efficiency and horsepower data from 50 individual cars to create a sample size of data for each car in the class type. So if there are 10 cars in each class type, I would have 500 data points collected for each fuel efficiency and horsepower.

What metric or metrics are you going to test?
What is the null hypothesis or alternative hypothesis?
What statistical test would you use to test the hypothesis? And why? We want to know the p value????
What data is needed to run the statistical test?


----

**Completed by:** Jennifer Anno-Kusi

**Email:** jannokusi@gmail.com 
