# Hitch-Hiker's-Travel-Guide
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)

## Goal | Problem statement 🥇
We all like to travel. There are some people who plan trips and others leave on a whim without tangible plans.   
For this project, my goal was to provide information and provide a summary which will help out target audience make effective decisions while travelling.

## Target Audience 🎯
  - Hitch Hikers 🥾. 
  <!--- ![Hitch hikers](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Group%201.png)-->
  <img width="500" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Group%201.png">
  - Holiday makers 🏖️.  
  <!--- ![Holiday makers](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Group%202.jpg)-->
  <img width="500" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Group%202.jpg">


### Summary description of the data used for the project
  Data for this project is taken from [Numbeo](https://www.numbeo.com/cost-of-living/) _a crowd-sourced cost of living database_ for the year 2021.  
 After gathering the data; I did some transforms and merges to end up with the final dataset.   
 
 **Tools used**:  
  - 📕 Notebook and 🖋️ Pen   
  - 🐍 Python [Data manipulation]   
  - Adobe Illustrator [Visualization]   
  - Tableau

## Approach
  - Merged multiple sheets,
  - Converted columns to categorical where necessary.  
  [_Notebook_](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/main/notebooks/manipulations.ipynb)
___

1. **Transportation 🚍**  
  Normally, I will assume Climate Index and Pollution Index have an effect on commute time.  
  So i decided to check the correlation and covariance of Traffic Commute Time Index, Pollution Index and Climate Index.  
  I noticed the _covariance of_:
    - Traffic Commute Time Index and Pollution Index: 0.9020864451308938.  
    - Traffic Commute Time Index and Climate Index: 0.8992827901260081.  
  So these 2 variables are linearly related to Traffic Commute Time Index as earlier assumed.  
  In the course of manipulating the data I noticed some NULL values and decided to filter out those countries.   
  [👉 Resulting Dashboard ](https://public.tableau.com/profile/quinsy.brenda#!/vizhome/HowPollutionandClimateIndexInfluenceTrafficCommuteTime/Dashboard1)  
  <!--- ![Result](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%201.png)-->
  <img src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%201.png" />

2. **Lodging 🏚️**   
  For Lodging I considered the 
    - Country 
    - Rent Index
    - Groceries Index
    - Property Price to Income Ratio
    - Local Purchasing Power Index.   
  columns.  
  I thought these 3 variables should influence choice when going for a place to stay.  
  The data here had 138 countries considered here.  
  [👉Resulting Dashboard](https://public.tableau.com/views/LodgingCosts/Dashboard2?:language=en&:display_count=y&:origin=viz_share_link)
  <!--- ![Result Lodging](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%202.png)-->
  <img src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%202.png" />

3. **Safety 👮**   
  It made sense to me that Safety should be influenced by traffic commute time.     
  I wanted to look at the correlation of traffic commute and safety and got a value of -0.5475, which seems to me like they are inversely related.  
  So i chose to plot it ...   
    - <img width="300" alt="image" src="https://user-images.githubusercontent.com/28558929/112666408-72421180-8e5c-11eb-9015-1799211953a1.png">
    - [👉Resulting Dashboard](https://public.tableau.com/views/SafetyandCommuteTime/Dashboard3?:language=en&:display_count=y&:origin=viz_share_link)  
    <!--- ![Result Safety](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%203.png)--->
    <img src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%203.png" />
  
4. **Weather 🌦️**  
  How often does the weather change? Some countries have super spontaneous waether while others are more predictible.  
5. **Food 🥖**   
  After looking considering groceries under lodging, Food here considers just fancy dining and eating out.  
  As usual with these assumptions, I think the restaurant prices should be influenced by climate index and safety.  
  However, plotting these;   
    - <img width="370" alt="image" src="https://user-images.githubusercontent.com/28558929/112664128-e929db00-8e59-11eb-93a4-e39cd07ee3b1.png">
  From the plots I don't see any statistical proof of linearity between the variables.
  I didn't trust the plots so I calculated the correlation cooefficient :    
    - Restaurant Price Index, Safety Index: 0.27162826173619786   
    - Restaurant Price Index, Climate Index: 0.2014795908896057    
  [👉Resulting Dashboard](https://public.tableau.com/views/RestaurantPricing/Dashboard1?:language=en&:display_count=y&:origin=viz_share_link)
  <!--- ![Resulting Food](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%201-2.png)--->
  <img src=" https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%201-2.png" >
 
  
## Links to Tableau Results
  - [Traffic Commute](https://public.tableau.com/profile/quinsy.brenda#!/vizhome/HowPollutionandClimateIndexInfluenceTrafficCommuteTime/Dashboard1)
  - [Restaurant Prices and Weather](https://public.tableau.com/views/RestaurantPricing/Dashboard1?:language=en&:display_count=y&:origin=viz_share_link)
  - [Safety](https://public.tableau.com/views/SafetyandCommuteTime/Dashboard3?:language=en&:display_count=y&:origin=viz_share_link) 
  - [Lodging](https://public.tableau.com/views/LodgingCosts/Dashboard2?:language=en&:display_count=y&:origin=viz_share_link)
  
## Conclusions and next steps
It would be helpful to dig deeper into the data, get a more complete and recent dataset to improve on the information.

