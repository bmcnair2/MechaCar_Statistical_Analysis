# MechaCar_Statistical_Analysis
Statisitical analysis of automobile performance with R

## Overview
AutosRUs' new MechaCar is struggling with production troubles and the company is hoping that an analytical review may help give insight. The goal of this project is to:
* discover which variables predict the MPG for vehicles;
* gather summary stats on the PSI of suspension coils;
* determine if manufacturing lots are statistically different from the mean population;
* create a study to compare the MechaCar performance against competing vehicles.

## Results

### Linear Regression to Predict MPG
![Multiple Linear Regression on MPG](mpg_line_regres_summry.png)

* The most significant variables in our dataset which show a non-random effect on the MPG of the MechaCar are the Vehicle Length and the Ground Clearance. As indicated with yellow arrows in the image above, a linear regression on these variables against figures for MPG, resulted in p-values of 2.6x10<sup>-12</sup> and 5.21x10<sup>-8</sup>, respectively. The intercept was also statistically significant, indicating there are likely other factors outside of our dataset that have a strong impact on the MPG.
* The slope of the linear model can not be considered to be zero, as the p-value of 5.35x10<sup>-11</sup>, indicated with the orange arrow, is lower than even an extreme level of significance, and thus the null hypothesis must be rejected. This means that the relationship between our variables and the miles per gallon is subject to more than random chance.
* Although there unconsidered factors exist, this model does predict the mpg of the MechaCar prototype with relative effectiveness. The r-squared value of 0.7149, highlighted in the purple box, indicates that the model is 71% accurate.

### Summary Statistics on Suspension Coils
![Suspension Coil Total Summary](sus_coil_tot_sum.png)
![Suspension Coil Lot Summary](sus_coil_lot_sum.png)
* While the overall variance, as shown in the Total Summary data above, is under 100 psi and meets specifications, there is a problem with one of the individual lots. As shown in the Lot Summary stats, the variance for Lot 3 is well over the acceptable threshold, at 170.28.

### T-Tests on Suspension Coils
Suspension Coils Cumulative T-test
![Suspension Coils Cumulative T-test](sus_coil_one_samp_ttest.png)
* A review of the results of the T-test for the suspension coils across all manufacturing lots shows that they are not statistically different from the population mean, and the p-value is not low enough (0.0603) for us to reject the null hypothesis.
![Suspension Coil Lot 1 T-test](sus_coil_lot1_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 1 shows that they are not statistically different from the population mean, and the p-value is not low enough (1) for us to reject the null hypothesis.
![Suspension Coil Lot 2 T-test](sus_coil_lot2_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 2 shows that they are not statistically different from the population mean, and the p-value is not low enough (0.6072) for us to reject the null hypothesis.
![Suspension Coil Lot 3 T-test](sus_coil_lot3_samp_ttest.png)
* A review of the results of the T-test for the suspension coils for Lot 3 shows that they are slightly statistically different from the population mean, and the p-value is just low enough (0.0417) for us to reject the null hypothesis. This lot may be need to be discarded, or at least more closely evaluated.

## Study Design: MechaCar vs Competition
Many factors are considered when deciding which car to purchase. There are many options for affordable travel and customers are looking to purchase a car for more than just a transportation. Consumers are looking to purchase a car that is an economical means to regularly transport themselves and their items on a reliable, regular basis.
### Metric to test
To narrow down the test, we should evaluate MechaCar's carrying capacity, in cubic inches, in comparison to various competitors' vehicles.
### Null and Alternate Hypothesis
H<sub>0</sub>: MechaCar prototypes' average carrying capacity is similar to competitor's vehicles in the same vehicle class
H<sub>a</sub>: MechaCar prototypes' average carrying capacity is statistically above or below that of competitor vehicles.
### Statistical Test Used
Two-sample t-tests.
### What data is needed
Gathering cubic space data from the carrying compartments of all MechaCar prototypes, as well as from all major competitor vehicles would be needed.
