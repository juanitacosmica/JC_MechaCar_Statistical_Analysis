# JC_MechaCar_Statistical_Analysis
Module 15: Statistics and R

# Overview of the analysis:

In this challenge, a multiple linear regression analysis was performed to identify which variables in the dataset predict the mpg of MechaCar prototypes, collected summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots, ran t-tests to determine if the manufacturing lots are statistically different from the mean population, designed a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, there is a summary interpretation of the findings.

4 parts were accomplished:

- D1: Linear Regression to Predict MPG
- D2: Summary Statistics on Suspension Coils
- D3: T-Test on Suspension Coils
- D4: Design a Study Comparing the MechaCar to the Competition

# Resources:
 
  **Data source** 2 csv files have been used in this analyses and available in the [Data Folder](https://github.com/juanitacosmica/JC_MechaCar_Statistical_Analysis/tree/main/Data)

  **Software** R Studio.

# Analysis of the Results:

## 1. Linear Regression to Predict MPG

![D1_Linear_Regression](/Resources/D1_Linear_Regression.png)

  # 1.1 Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
      To determine which variables, we must look at their individual p-value; if the p-value is below 0.05 is not likely possible to provide random amounts of variance to the linear model, in other words, those variables have an impact on mpg. As per the results shown, the ground clearance (p-value = 5.21 x 10-8), vehicle length (p-value = 2.60 x 10-12), and the intercept (p-value = 5.08 x 10-8) provided a non-random variance to the mpg values in the dataset. When an intercept is significant, that means that there are other variables and factors contributing to the variation to mpg that were not included in the model. These variables may be in or not in the dataset and may still need to be sampled.

  # 1.2 Is the slope of the linear model considered to be zero? Why or why not?
      As per the results, the p-value is 5.35 x 10-11, which is smaller than the assumed significance level of 0.05%. Hence, it can be concluded that there is enough evidence to reject the null hypothesis; which indicates, that the slope of the linear model is different than 0, in other words, that there is a significant linear link between the variables and the mpg of the MechaCar prototype.

  # 1.3 Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
      It is necessary to look at the r-squared and p-value, to determine if this linear model helps predicting the mpg of MechaCar prototypes effectively. As per the results, r-squared is 0.7149 and indicates a strong positive linear link, hence, it can be confirmed that the linear model predicts the mpg of MechaCar prototypes.

![D1_P_and_R2_Values](/Resources/D1_P_and_R2_Values.png)

## 2. Summary Statistics on Suspension Coils

  # 2.1 The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

  # 2.1.1 All lots
        The manufacturing data meet the design specification for all manufacturing lots in total. As per the results, the variance is 76.23 PSI which is within requirements and not above the variance of 100 PSI.
        
  ![Total Summary](/Resources/D2_Total_Summary.png)

  # 2.1.2 Each lot individually
        The manufacturing data partially meet the design specification for each lot separate. As per the results, the Lot 1 and Lot 2 meet the design specification with a variance of 1.15 and 10.13 PSI accordingly, and it is within requirements and not above the variance of 100 PSI. While the Lot 3 does not meet the design specification, because of its variance of 220.01 PSI that exceeds the requirements variance of 100 PSI.
        
  ![Lot Summary](/Resources/D2_Lot_Summary.png)

## 3. T-Tests on Suspension Coils

The t-test performed is used to determine if there is a statistical difference between the means of the sampled suspension coil data and the population dataset with a given mean of 1,500 PSI. With the t-test, it is stablished the following hypothesis:

- H0: There is no statistical difference between the suspension coil data set mean and its population mean is 1,500 PSI.
- Ha: There is statistical difference between the suspension coil data set mean and its population mean is 1,500 PSI.

The fail criteria to reject the null hypothesis we must look at the p-value to determine whether there is a statistical difference between the observed sample mean and its population mean. As per the results, the p-value for all manufacturing lots is 0.5117, for lot 1 = 0.9048, for lot 2 = 0.3451, and for lot 3 = 0.637. Overall, the p-value is over the assumed significance level of 0.05. Hence, there is not enough evidence and we fail to reject the null hypothesis, in other words, the 2 means are not statistically different.

![All Lots](/Resources/D3_All_Lots.png)
![Lot 1](/Resources/D3_Lot1.png)
![Lot 2](/Resources/D3_Lot2.png)
![Lot 3](/Resources/D3_Lot3.png)

## 4. Study Design: MechaCar vs Competition

  # 4.1 What metric or metrics are you going to test?
      Electric vehicles are in high demand as customers are more concerned about the environment and are suffering the impact of rising fuel prices. However, many car users are not ready to invest in an electric vehicle for various reasons, MechaCar can provide good alternatives. That being said, testing metrics such as: a comparison of a single dependent variable exhaust system emissions means across a single independent variable transmission efficiency with multiple groups, with the competitors’ data.

  # 4.2 What is the null hypothesis or alternative hypothesis?
      To compare MachaCar against competition an analysis can be used the following hypotheses:
        - H0: The means of exhaust system emissions of all groups are equal.
        - Ha: At least one of the means of exhaust system emissions that is different from all other groups.

  # 4.3 What statistical test would you use to test the hypothesis? And why?
      One-way ANOVA test can be used to test the hypotheses, this is also known as Analysis of Variance and can be used to test the means of a single dependent variable across a single independent variable with multiple groups. For instance, the exhaust system emissions of different cars based on transmission efficiency; if the null hypothesis is rejected, it can be concluded that at least one of the means of exhaust system emissions is different from all other groups.

  # 4.4 What data is needed to run the statistical test?
      Data from:
      - Vehicle ID
      - Exhaust system emissions data
      - Transmission efficiency data
      Given the above input data should be validated prior to running statistical test:
      - The dependent variable is numerical and continuous, and the independent variables are categorical
      - The dependent variable is considered to be normally distributed
      - The variance among each group should be very similar.


People call me JC, the short for [Juanita C. Nunez](https://www.linkedin.com/in/juanitacamargonunez/). Contact me for any questions! I love networking, so here you go  my [LinkedIn] (https://www.linkedin.com/in/juanitacamargonunez/) :)


