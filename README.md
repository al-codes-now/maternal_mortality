# Maternal Mortality in the United States - A Regression Analysis 

![img](./images/preg_belly.jpeg)

### Using regression analysis to learn more about the rising rate of maternal mortality in the United States 

**Author**: [Alexandra Bruno](mailto:alexandrabruno7898@gmail.com)

## Overview

Maternal mortality has been on an upward trend over the past several years. The Center of Disease Control and Prevention has stated the exact cause as to why this is occurring is still unknown. The purpose of this statistical analysis is to help us gain a better understanding as to why this may be occuring, and what factors have a larger impact on maternal mortality versus others. 

## Business Problem 

Preventable maternal death is a problem that occurs all over the globe. Although maternal death is less severe in the U.S. in comparison to underdeveloped countries, it is still an ongoing problem that we are faced with in the states. No mother should pass on what is supposed to be one of the most important days of her life. With statistical analysis we can see what are some indicators there contribute to higher rates of maternal mortality. 

## Data

The data was obtained from three different sources, including 

- The Global Health Data Exchange
- The Center of Disease control and Prevention
- The Census Bureau.

I was able to scrape the data from the CDC using selenium. There is an option to export the data to a csv file, but the size of the dataset I was requesting was very large and it would not export. I was able to get the census data with several API calls. The Data from the Global Health Data Exchange was easy to obtain, I just selected the parameters for my dataset on their website and I was emailed a downloadable link. After cleaning and processing the data I merged the three sets on my AGE, STATE, and YEAR variables. 

My variables and description are as listed below. My target variable is DEATH_RTE


![img](./images/variables.jpg)

## What does the data look like?

Below we can get an idea of how the maternal death rate is distributed among the different age groups

![img](./images/histogram.png)

![img](./images/boxplot.png)

This graphs show us that women in the older age ranges experience higher rates of maternal death. This is too be expected, as women who give birth at older ages are at increased risk for adverse outcomes during pregnancy. Additionally, we can see that the younger age ranges, especially 15-19 year olds, do not contribute to maternal death nearly as much. 

## Methods 

For this regression analysis I chose to run an Ordinary Least Squares model. For evaluating where or not my variables impact the maternal death rate I am prioritizing p-values and R-squared and Adj. R-squared as an evaluation metric. In this model I controlled for age and state.

I ran multiple models which can be found in the modeling notebook. I tested each of my independent variables against the dependent variable individually, however I found these results to be biased since this showed each IV being statistically significant. 

## Results

Below are the results from my baseline OLS model, which produced the highest R-squared and Adj. R-squared. 

![img](./images/results_1.jpg)


![img](./images/results_2.jpg)

The p-values of the variables below indicate statistical significance at the 95% significance level

- RTE_GON - negative impact on the DEATH_RTE

- PRC_BLK - negative impact on the DEATH_RTE

- PRC_WHT - negative impact on the DEATH_RTE

- PRC_HISP - positive impact on the DEATH_RTE

- fifteen_nineteen - negative impact on the DEATH_RTE

- twnty_twntyfour - positive impact on the DEATH_RTE

- twntyfiv_twntynine - positive impact on the DEATH_RTE

- thrtyfiv_thrtynine - positive impact on the DEATH_RTE

It is not surprising that the older groups of women are impacting the maternal death rates more in comparison to the younger groups. It is important to note that the percent of white and black fertile women impact the maternal death rate disproportionally. 

## Conclusion and Suggestions

The results of the model suggests that different racial groups impact maternal mortality at disproportionate rates. Additionally, older women contribute to the maternal death rate the most. Going forward, more research should be conducted to help us better understand these relationships. Additionally, older women and those belonging to racial minority groups should receive additional care and more steps should be taken to help prevent maternal death in the future. 

## Future Research 

In the future I would like to get data on an individual basis. I think it would be helpful to cluster women with similar medical history and try to predict the probability of them experiencing maternal death or not. I think taking into account factors such as obesity and smoking can also help to give us a clearer picture about these relationships. 

## Repo Structure 

images - images found in the readme 

Final Notebooks - cleaned and finalized notebooks

Gitignore - working notebooks 

