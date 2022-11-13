# Assignment 5.1 Readme

Objective: The goal is to analyze the data for demographics and behavioral patterns to identify the right target customers who are most likely to accept coupons. 

Data Set: The dataset contained information about passengers who were given coupons (with information around time of day, weather, expiration) as well as demographic information (age, marital status, children, education, occupation etc) and the type of coupons (bar, coffee or carry away) and how much they are willing to spend at restaurant and direction of travel. With this we are trying to determine if the driver is willing to accept or use a certain type of coupon.

Data Cleansing: The dataset was loaded and checked for any correlations amongst the numeric values, checked for nulls and missing values in the columns and anything else that stood out. The findings were that numerical columns did not have much correlation with another. There was a large amount of missing data in the car column which did not seem relevant for analysis and hence dropped from the dataset. Rest of the dataset had a significantly small impact of missing data. Analysis was done on the data values missing and assigned to the value type that had the highest count.  

Data Analysis: An overall analysis shows that coupon acceptance rate is nearly 57%. Further analysis showed that cheaper options like CoffeeHouse or Restaurants(<20) had higher acceptance rate than more costly options like bars or Restaurants (20-50). Also, analyzed the temperature column that showed the highest coupons accepted when the temperature was in the 80s and weather was Sunny. 

Acceptance rate analysis for Bar Coupons: For this analysis, different scenarios were created considering the frequency of bar visits. For this a new frequency function was created to calculate frequency of bar visits (less than 3 times a month to more than 3 times).Drivers who had lower frequency of bar visits of less than 3 times per month accepted coupons over those who visited more than 3 times per month by an overwhelming majority. Further scenarios were considered by changing the frequency of visits to more than once a month or less. Analysis showed that drivers who are likely to accept bar coupons were people who went to bars more than once a month and did not have passengers who were kids.

Acceptance rate analysis for Coffee Coupons: Similar analysis was done on drivers accepting CoffHouse coupons. 

Additional analysis of target customers: Overall analysis on other demographics situations to see if gender, having children or marital status lead to higher acceptance. Females with married partners, having children or male singles with no children accepted the highest number of coupons. Further 'Sunny' weather, '1d' expiration and evenings '6PM' had the highest influence on drivers accepting coupons. Lastly, people with income levels above $50000, working in Professionals/Business/Workers and degree holders had the highest propensity to accept a coupon.

https://github.com/krana002/UCB_MLAI/blob/main/UCB_Assignment5.1_Final.ipynb
