# Hitch-Hiker's-Travel-Guide
[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)

## Goal | Problem statement 🥇
We all like to travel. There are some people who plan trips and others leave on a whim without tangible plans.   
For this project, my goal was to provide information and provide a summary which will help out target audience make effective decisions while travelling.

## Target Audience 🎯
  - Hitch Hikers 🥾. 
  <!--- ![Hitch hikers](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Group%201.png)-->
  <img width="1920" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Group%201.png">
  - Holiday makers 🏖️.  
  <!--- ![Holiday makers](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Group%202.jpg)-->
  <img width="1920" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Group%202.jpg">

## What have others done?
Numbeo is a cost of living database. It is a crowd-sourced global database of quality of life data including housing indicators, perceived crime rates, healthcare quality, transport quality, and other statistics.   
<img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/183379570-64f54692-d2e3-47e7-9700-ba102c20fd20.png">   
Though the data is available on Numbeo and is reliable becuase the data is provided by the population, the issue I find with the platform is the difficulty of use. To use this platform, the user has to navigate the map to get a summary statistic after for a particular indicator.   
With this project, I hope to provide a prototype of a platform which provides more insights which are more readily available and easier to access.   


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
  [_Notebook_](https://notebooks.githubusercontent.com/view/ipynb?azure_maps_enabled=true&browser=safari&color_mode=dark&commit=034a486567c531ea50a040e45bfcafa03be3bf0c&device=unknown_device&enc_url=68747470733a2f2f7261772e67697468756275736572636f6e74656e742e636f6d2f6c61676f6d2d51422f48697463682d48696b65722d732d54726176656c2d47756964652f303334613438363536376335333165613530613034306534356266636166613033626533626630632f6e6f7465626f6f6b732f646174615f6d616e692e6970796e62&logged_in=true&nwo=lagom-QB%2FHitch-Hiker-s-Travel-Guide&path=notebooks%2Fdata_mani.ipynb&platform=mac&repository_id=348869685&repository_type=Repository&version=15#7697cf86-401c-421f-b6f1-6ddd119fd374)
___

1. **Transportation 🚍**  
  Normally, I will assume Climate Index and Pollution Index have an effect on commute time.  
  So I decided to check the correlation and covariance of Traffic Commute Time Index, Pollution Index and Climate Index.  
  I noticed the _covariance of_:
    - Traffic Commute Time Index and Pollution Index: 0.9020864451308938.  
    - Traffic Commute Time Index and Climate Index: 0.8992827901260081. 
  So these 2 variables are linearly related to Traffic Commute Time Index as earlier assumed.  
  In the course of manipulating the data I noticed some NULL values and decided to filter out those countries.   
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/183383198-fe424112-c36e-4de9-81db-235fcc682be2.png">
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/183383492-862c9a5e-f6ca-49ab-a134-ac416cd1537b.png">

  [👉 Resulting Dashboard ](https://public.tableau.com/profile/quinsy.brenda#!/vizhome/HowPollutionandClimateIndexInfluenceTrafficCommuteTime/Dashboard1)  
  <!--- ![Result](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%201.png)-->
  <img width="1920" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%201.png" />

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
  <img width="1920" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%202.png" />

3. **Safety 👮**   
  It made sense to me that Safety should be influenced by traffic commute time.     
  I wanted to look at the correlation of traffic commute and safety and got a value of -0.5475, which seems to me like they are inversely related.   
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/183383979-8b3abe83-08a6-4677-8711-db61d481bd08.png">

  So i chose to plot it ...   
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/112666408-72421180-8e5c-11eb-9015-1799211953a1.png">
  [👉Resulting Dashboard](https://public.tableau.com/views/SafetyandCommuteTime/Dashboard3?:language=en&:display_count=y&:origin=viz_share_link)  
  <!--- ![Result Safety](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%203.png)--->
  <img width="1920" src="https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%203.png" />
  
4. **Weather 🌦️**  
  How often does the weather change? Some countries have super spontaneous weathers while others are more predictible.
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/183384205-f7feaeef-551e-4b9c-a177-397583ce41e7.png">
5. **Food 🥖**   
  After looking considering groceries under lodging, Food here considers just fancy dining and eating out.  
  As usual with these assumptions, I think the restaurant prices would be influenced by climate index and safety.  
  However, plotting these;   
  <img width="1920" alt="image" src="https://user-images.githubusercontent.com/28558929/112664128-e929db00-8e59-11eb-93a4-e39cd07ee3b1.png">
  
  
  From the plots I don't see any statistical proof of linearity between the variables.
  
  I decicided to be extra sure and calculate the correlation coefficient :    
    - Restaurant Price Index and Safety Index have a correlation coefficient of _0.27162826173619786_.  
    - Restaurant Price Index and Climate Index have a correlation coefficient of _0.2014795908896057_.   
    
    
  [👉Resulting Dashboard](https://public.tableau.com/views/RestaurantPricing/Dashboard1?:language=en&:display_count=y&:origin=viz_share_link)
  <!--- ![Resulting Food](https://github.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/blob/gh-pages/Dashboard%201-2.png)--->
  <img width="1920" src=" https://raw.githubusercontent.com/lagom-QB/Hitch-Hiker-s-Travel-Guide/gh-pages/Dashboard%201-2.png" >
 
  
## Links to Tableau Results
  - [Traffic Commute](https://public.tableau.com/profile/quinsy.brenda#!/vizhome/HowPollutionandClimateIndexInfluenceTrafficCommuteTime/Dashboard1)
  - [Restaurant Prices and Weather](https://public.tableau.com/views/RestaurantPricing/Dashboard1?:language=en&:display_count=y&:origin=viz_share_link)
  - [Safety](https://public.tableau.com/views/SafetyandCommuteTime/Dashboard3?:language=en&:display_count=y&:origin=viz_share_link) 
  - [Lodging](https://public.tableau.com/views/LodgingCosts/Dashboard2?:language=en&:display_count=y&:origin=viz_share_link)
  
## Conclusions and next steps
From these results, I would say:
- Climate Index and Pollution Index are linearly related to Traffic Commute Time Index. 
- Rent Index, Groceries Index, Property Price to Income Ratio and Local Purchasing Power Index have no statistical proof of linearity.  
The resulting platform would provide summary data for the user.   
<img width="960" alt="image" src="https://user-images.githubusercontent.com/28558929/183395920-e5bca9df-d853-43f0-be88-b4fd09eb6ce5.png">
<img width="339" alt="image" src="https://user-images.githubusercontent.com/28558929/183397178-968eed7b-6d0f-44cc-87fb-acf5647b00bc.png">


In the future, I hope to provide an MVP of the product, get access to an api through which to pull the data from and automate the process.

