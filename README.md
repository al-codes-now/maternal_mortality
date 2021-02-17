# Maternal Mortality in the United States - A Regression Analysis 

![img](./images/pregnancy.jpg)

### Using regression analysis to learn more about the rising rate of maternal mortality in the United States 

**Author**: [Alexandra Bruno](mailto:alexandrabruno7898@gmail.com)

## Overview

Maternal mortality has been on an upward trend over the past several years. The Center of Disease Control and Preventation has stated the exact cause as to why this is occuring is still unknown. The purpose of this statistical analysis is to help us gain a better understanding as to why this may be occuring, and what factors have a larger impact on maternal mortality verses others. 

## Business Problem 

Preventable maternal death is a problem that occurs all over the globe. Although maternal death is less severe in the U.S. in comparison to underdeveloped countries, it is still an ongoing problem that we are faced with in the states. No mother should pass on what is supposed to be one of the most important days of her life. With statistcal analysis we can we what are some indicators there contribute to higher rates of maternal mortality. 

## Data

The data was obtained from three different sources, including the Global Health Data Exchange, the Center of Disease control and Prevention, and the Census Bureau.
I was able to scrape the data from the CDC using selenium. There is an option to export the data to a csv file, but the size of dataset I was requesting was very large and it would not export. I was able to get the census data with several API calls. The Data from the Global Health Data Exchange was easy to obtain, I just selected the paramaters for my dataset on their website and I was emailed a downloadable link. After cleaning and processing the data I merged the three sets on my AGE, STATE, and YEAR variables. 
