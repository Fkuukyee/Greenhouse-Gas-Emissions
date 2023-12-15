# Modelling Greenhouse Gas Emissions in the Canadian Industrial Sector using Economic out and Energy usage.
  By Frank Kwaku Kuukyee and 	Olayinka Soremekun 

## Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Tools](#tools)
- [Workflow](#workflow)
- [Main ResultsS](#main-results)
- [Interpretations of coefficients](#interpretations-of-coefficients)
- [Test for Assumptions](#test-for-assumptions)
- [Conclusion and Discussions](#conclusion-and-discussions)
- [Future Work](#future-work)
- [Reference](#reference)
  
## Project Overview
The environmental impact of industrial activities is a global concern as nations strive to achieve sustainable development and mitigate climate change.Moreover, industries play a crucial role in contributing to the nation’s economic growth, but it also contributes to greenhouse gas emissions. This project provides an understanding of the interaction between the two pivotal factors—Gross Domestic Product (GDP) and Energy Usage in predicting Greenhouse gas emissions.

## Data Source
The data was obtained from the website of Natural Resources Canada. Data was collected on Green House Gas emission measured in Metric Tonnes of CO2 equivalent [Mt.CO2e], Energy consumption in Peta Joules[PJ] and Activity in Gross Domestic Product (GDP) for the major industries in Canada between 2017 and 2020. Average values were calculated for the Green House Gas emission, Energy consumption and GDP between 2017 and 2020. The Greenhouse gas emissions [Mt.CO2e] were converted to CO2 equivalent [CO2e] to increase the significant figures.

![image](https://github.com/Fkuukyee/Greenhouse-Gas-Emissions/assets/147086232/e47e2574-15f1-4fcb-ba91-cf3fb0067310)

## Tools
- Microsoft Excell for data pre-cleaning
- Python Pandas for data cleaning andanalysis
- R-studio for statistical modelling and analysis
- Microsoft word for report writting

## Workflow
1.	Data Preprocessing: Handle missing values, scale features as required
2.	Exploratory Data Analysis (EDA): Understand data distributions, identify outliers, and explore correlations.
3.	Model Selection: Identify the most relevant predictors for inclusion in the regression model.
4.	Model Evaluation: Assess model performance using relevant metrics such as R-squared, Mean Squared Error, individual T-test and partial F-test.
5.	Interpretation of Results: Analyze coefficients and make inferences about the impact of economic output and energy usage on greenhouse gas emissions

## Main Results
After evaluating the full, higher order and interactive models using individual t-tests and partial F-tests, the Interactive model does contribute significantly to explaining the variance in the response variable (Emissions) compared to the other Models. Our best model for predicting Greenhouse emissions is shown below.

![image](https://github.com/Fkuukyee/Greenhouse-Gas-Emissions/assets/147086232/599ae439-324d-45b5-a85b-84e97ff482c1)

### Interpretations of coefficients

![image](https://github.com/Fkuukyee/Greenhouse-Gas-Emissions/assets/147086232/914fde5d-d70f-41ab-86f0-5a063028b681)

- Intercept (β0 ): The estimated intercept is 1209. However, its p-value is 0.36285, which is greater than the significance level of 0.05. This suggests that the intercept is not significantly different from zero, and it might not be a meaningful parameter in explaining the variance in emissions.
- Energy (β1): The estimated coefficient for Energy is 27.53. This implies that, holding GDP constant, a one PJ increase in Energy consumption is associated with an estimated increase of 27.53 CO2e. The p-value (0.00236) is less than 0.05, indicating that the coefficient for Energy is statistically significant.
- GDP (β2): The estimated coefficient for GDP is r -0.01661. This suggests that, holding Energy constant, a million $2012 increase in GDP is associated with an estimated decrease of 0.01661 CO2e in Emissions. However, the p-value (0.52381) is greater than 0.05, indicating that the coefficient for GDP is not statistically significant. Therefore, GDP might not be a significant predictor in the model but It is kept for the hirachical rule.

## Test for Assumptions 
The model was tested for the following assumptions which it passed
- Linearity and Independence using residuals and fitted plots
- Normality using histogram and Q-Q plots of the residuals, and Shapiro-Wilk test
- Equal Variance using residuals and scale-location plots, and the studentized Breusch-Pagan test
- Multi-colinearity with pair plots and variance inflation factor
- Influential Points and Outliers with residuals vs leverage plot and cook's distance

## Conclusion and Discussions
The model's output, demonstrates the significant impact of both Energy and the interaction term Energy: GDP on greenhouse gas emissions.The coefficients indicate that both Energy and the interaction term Energy: GDP have statistically significant effects on greenhouse gas emissions. The Adjusted R-squared of 0.967 demonstrates the model's high explanatory power, capturing approximately 96.7% of the variance in emissions. Moreover, the model's adherence to various assumptions, including linearity, independence, normality, equal variance, multicollinearity, and outliers, provides confidence in its robustness. 

## Future Work
The success of the model opens avenues for future work. While the present study focused on the main predictors, additional variables such as industrial sector specifics and technological advancements could further enhance the model's accuracy. 

## Reference
Canada, E. A. C. C. (2023). Greenhouse gas emissions. Canada.ca. https://www.canada.ca/en/environment-climate-change/services/environmental-indicators/greenhouse-gas-emissions.html
