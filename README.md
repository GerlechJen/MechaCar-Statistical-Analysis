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
T-Test across all lots 
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/All_Lots.png)

T-Test across Lot 1
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot1.png)

T-Test across Lot 2
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot2.png)

T-Test across Lot 3 
![image](https://github.com/GerlechJen/MechaCar_Statistical_Analysis/blob/main/Images/Lot3.png)


