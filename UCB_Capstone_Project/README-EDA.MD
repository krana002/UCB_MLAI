# UCB Capstone Project - EDA

### By: Kaushik Rana

Business Understanding
In this decade, when climate change and rising global temperatures has a huge impact on planet earth (melting glaciers, rising sea levels and intense heat waves), this project is aimed at gaining a greater understanding how the temperatures changed over the past 50 years. Using the global average temperature data (both from land and sea) from 1743 to 2013 to analyze any trend, seasonality or cyclicality. Which years had the highest increase in temperature in the last few years ? What was the min, max and variance ? Based on past years data, could we predict temperature for future years?

Data Understanding
In order to answer the business question, am using the data from kaggle that has the temperature data on a monthly basis from 1750 and the following features. The data needs to be cleansed and transformed to be used in the analysis.

Data Features
Date: starts in 1750 for average land temperature and 1850 for max and min land temperatures and global ocean and land temperatures 
LandAverageTemperature: global average land temperature in celsius 
LandAverageTemperatureUncertainty: the 95% confidence interval around the average 
LandMaxTemperature: global average maximum land temperature in celsius 
LandMaxTemperatureUncertainty: the 95% confidence interval around the maximum land temperature 
LandMinTemperature: global average minimum land temperature in celsius 
LandMinTemperatureUncertainty: the 95% confidence interval around the minimum land temperature 
LandAndOceanAverageTemperature: global average land and ocean temperature in celsius LandAndOceanAverageTemperatureUncertainty: the 95% confidence interval around the global average land and ocean temperature

Exploratory Data Analysis
Dataset has all numerical values. High Correlation exist among all the variables: LandAverageTemperature to LandMaxTemperature, LandMinTemperature, LandAndOceanAverageTemperature. So, clearly high correlation exists among the average, min, max and uncertaintly values of land and ocean which are plotted.

Data Preparation
Data was investigated for missing values and noted null data in many of the columns above including the main variable LandAverageTemperature. Also, null values are noted in rows before 1850. For the purpose of analysis, that data may not be much helpful in predicting future temperatures. Hence, removed from the data set. All monthly data from 1850 was used for further analysis and preparation. 

Since the data is provided at a monthly level, we checked to see if the LandAveragetemperatures show seasonality and if we need to make special adjustments with that.
Plotting it showed that the temperatures increased consistenty across all the months of the year (increasing trend). So, if we take the average temperature for the year, that would be hepful for us to predict future temperatures and use in regression analysis.

Then checked how the key features LandAverageTemperature, LandMaxTemperature, LandMinTemperature and LandAndOceanTemperature trend over time (across centuries). It was observed that all the features show similar trends over the years. So, if the yearly LandAverageTemperature is used, it can be helpful for predicting future temperatures. Also, checked on seasonality and cyclical nature of the data using LandAverageTemperature. 

The land average temperature was plotted over the years and a straight line as fitted using linear regression. However, it was noted that the land average temperature increased significantly from 1960 onwwards and hence a straight regression line cannot be used for predicting the future temperatures from 1850. Replotted the above graph using lowess and see that the trend line curves upwards from 1960 onwards. Hence, for purpose of final dataset, yearly data from 1960 onwards will be used for linear and logistic regression analysis.

In order to analyze and categorize the data, it is important to find the temperature changes y-o-y and see which years had the highest increase or decrease. 
Hence, calculated and plotted the same with different shades of colors - the red color indicated the years when temperature increased above 0.2 degrees centigrae, green indicates if decreased below 0.2 degrees centigrade, and yellow indicates if the data increased or decreased within 0.2 degrees centigrade.

