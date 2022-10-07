# MechaCar_Statistical_Analysis

## Overview

The goal is to assess production issues that are obstructing the manufacturing process. The analysis will be conducted in R. The analysis will review and analyze the production data of the manufacturing lots to help resolve the issue.

There are four parts to the project:

1.	Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
2.	Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
3.	Run t-tests to determine if the manufacturing lots are statistically different from the mean population
4.	Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you'll write a summary interpretation of the findings.

## 1. Linear Regression to Predict MPG

For the first section, a multiple linear regression analysis was completed to determine which variables predict the mpg of MechaCar prototypes. The result was output using ```summary()``` to determine the p-value and the r-squared value for the linear regression model.

<img width="771" alt="Deliveralbe 1 lm" src="https://github.com/nfujikad/MechaCar_Statistical_Analysis/blob/main/Resources/deliverable_1.png">

<img width="771" alt="Deliverable 1 lm summary" src="https://github.com/nfujikad/MechaCar_Statistical_Analysis/blob/main/Resources/deliverable_1_1.png">

- **Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**

   In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According to the results, vehicle_length and ground_clearance have the smallest Pr(>|t|) values. This means vehicle_length and ground_clearance are statistically least likely to provide random amount of variance to the mpg value since they have significant impact on mpg values.

- **Is the slope of the linear model considered to be zero? Why or why not?**

   Results show the multiple linear regression model is:

    ```mpg = 6.267vehicle_length + 0.001245vehicle_weight + 0.06877spoiler_angle + 3.546ground_clearance – 3.411AWD – 104.0```

  The slope of the linear model cannot be considered as zero, as the coefficients for most of the variables are significant. In addition, the p-value of the linear regression analysis is 5.35e-11, which is much smaller than significance level of 0.05% (5e-4). Therefore, we can state that there is sufficient evidence to reject the null hypothesis, which in turn means that the slope of our linear model is not zero. 

- **Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**

    The linear regression summary shows the r-squared value is 0.7149, which means 71.49% of the variability of the dependent variable mpg is explained by the linear regression model. This number tells us that the linear model does predict mpg of MechaCar protypes effectively.