# Impact of Air Pollution and Socioeconomic Factors on Mortality Rates Across Countries

## Project Overview
This project investigates how air pollution levels (PM2.5) and socioeconomic indicators (such as GDP per capita and health expenditure) relate to mortality rates across countries. The goal is to analyze whether countries with higher pollution and lower economic well-being experience higher mortality.

## Motivation  

I’ve recently become more curious about how air pollution and economic conditions affect public health in different countries. Since these two factors vary a lot across the world, I wanted to understand whether they play a role in mortality rates. This project gives me a chance to explore that question using real data and the tools we learned in the course.

## Data Sources 
- PM2.5 Air Pollution Data: Annual fine particulate matter (PM2.5) concentrations for all countries. This dataset provides country-year pollution values used as the main environmental exposure variable. Collected from WorldBank.

- Income Level & Region Data: Contains country-level attributes such as income group (High, Upper-middle, Lower-middle, Low income) and geographic region classifications. These variables are used to analyze socioeconomic differences and compare mortality patterns across development levels.

- Mortality Data: Provides cause-specific and all-cause mortality estimates for each country. This dataset is used as the main health outcome variable to examine how air pollution exposure and income levels relate to mortality.

## Data Collection and Preparation
The datasets used in this project were obtained from two primary sources: the World Bank Data Portal and the Institute for Health Metrics and Evaluation (IHME).
After downloading, all datasets will be cleaned and converted into a consistent country–year structure. Country names and codes will be standardized to merge the datasets. The final merged dataset will include PM2.5 levels, income group classifications, and mortality rates for each country and year.

## Hypothesis
- Null Hypothesis 1 (H₀₁): PM2.5 levels do not have a significant impact on mortality rates across countries.
- Alternative Hypothesis 1 (Hₐ₁): Higher PM2.5 levels are associated with higher mortality rates across countries.
- Null Hypothesis 2 (H₀₂): Income level does not significantly affect mortality rates.
- Alternative Hypothesis 2 (Hₐ₂): Countries with lower income levels have higher mortality rates.
- Null Hypothesis 3 (H₀₃): Income level does not significantly affect PM2.5 exposure levels.
- Alternative Hypothesis 3 (Hₐ₃): Countries with lower income levels have higher PM2.5 exposure levels.

## EDA Process
I started the EDA process by gathering and combining three datasets: PM2.5 air pollution data from the World Bank (2020), mortality rates from the IHME Global Burden of Disease Study (2023), and country income classifications from the World Bank metadata.
Because PM2.5 measurements were only available up to 2020 and the mortality data was from 2023, I used the most recent year from each dataset. Since my analysis is cross-sectional, comparing countries at one point in time was enough for the goals of this project.
After merging everything using country codes and names, I cleaned the data by removing missing values and standardizing the income groups. The final dataset included 172 countries that had complete information for PM2.5 levels, mortality rates, and income categories.
Once the data was ready, I moved on to the visualization stage.


## Hypothesis Testing
To check whether the relationships I observed in the EDA were statistically meaningful, I ran hypothesis tests using Pearson correlation to test the relationship between PM2.5 and mortality, and one-way ANOVA to compare mortality rates and PM2.5 levels across different income groups. The significance level was set at α = 0.05.


## Hypothesis Test 1: PM2.5 vs Mortality Rate
- Pearson’s r: –0.339
- p-value: 0.0000055
- R²: 0.115
- Direction: Negative
- Conclusion: Reject H₀ (significant)

Interpretation: Countries with higher PM2.5 sometimes have lower mortality, but the relationship is weak. This likely reflects demographic differences rather than pollution directly lowering mortality. PM2.5 alone does not explain mortality well.

## Hypothesis Test 2: Income Groups – Mortality Rates
- F: 14.52
- p-value: 0.00000018
- η²: 0.206
- Conclusion: Reject H02 (Significant)

Interpretation: Mortality rates are significantly different across income groups. Income level explains about 21% of the variation. The main reason is demographics: high-income countries have older populations with higher natural mortality, while lower-income countries have younger populations.

## Hypothesis Test 3: PM2.5 Levels Across Income Groups
- F-statistic: 18.41
- p-value: 0.000000002
- Effect size (η²): 0.247
- Conclusion: Reject H₀₃ (Significant)

Interpretation: PM2.5 levels are significantly different across income groups. Income level explains about 25% of the variation in pollution exposure. Low-income countries face much higher air pollution than wealthy countries. This makes sense because wealthier nations have stricter environmental regulations, cleaner energy sources, and better pollution control technology.


## Visualization Stage
During the visualization stage, I looked at how PM2.5 levels, mortality rates, and income groups relate to each other.
- PM2.5 vs Mortality Rate:
There was a negative correlation between PM2.5 and mortality rates. Surprisingly, countries with higher pollution sometimes had lower mortality rates. This suggested that factors like healthcare quality or population age structure might be influencing the results.
- Income Groups – Mortality Rates:
High-income countries had the highest mortality rates, while lower-middle-income countries had the lowest. This likely reflects demographic differences—wealthier countries tend to have older populations, which naturally increases mortality.
- Income Groups – PM2.5 Levels:
Lower-income countries showed noticeably higher PM2.5 levels. Low-income countries had the highest average PM2.5 (around 40 µg/m³), while high-income countries had the lowest (around 15 µg/m³).
- Distribution Patterns:
Both PM2.5 and mortality rate distributions were right-skewed. Most countries were in moderate ranges, but a few had very extreme values.

