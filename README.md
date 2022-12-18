# DSLS Case Study  
### Analyze Yellow Taxi Operation over New York Area  

---

**Status**: Done  
**Dataset**: Here  
**Analysis on Jupyter notebook**: [Here](https://github.com/IchfanKurniawan/tlds-project/blob/master/code/tlds-project.ipynb)  
**Dashboard on Tableau Public**: [Here](https://public.tableau.com/app/profile/ichfan.kurniawan/viz/Whyisyellowtaxiconcentratinginmanhattan/Dashboard1?publish=yes)  
  

## Executive Summary  
The majority of New Yorkers depend on public transportation or taxi services. Despite the large-scale network of taxi services, the current system does not serve the boroughs equally. Because of this, residents prefer illegal taxi services that have inconsistent access and fares. This project analyzes the phenomena and brings recommendations that might solve the problem above.  

The analysis finds that in the given dataset the majority of taxi prefers to operate in Manhattan Borough than others. This could be indicated by the developed Tableau Dashboard that shows the market share of Manhattan Borough is almost 3 times higher than others, then the total of passengers is almost 7 times higher than others, and then the total records are almost 5 times higher than others.  

Two machine learning models (Logistic Regression & Random Forest Classifier) have been employed to find the most influential factors of the phenomena. The models show that economic factors (e.g. fare rate, the total amount of payment) are the most influential. The fare rate in Manhattan Borough ($ 5.8655 ± 9.8334) is higher than in other boroughs ($ 3.7927 ± 17.3213), and then the total amount of payment that they receive in Manhattan ($ 9.7783 ± 12.6916) is also higher than other boroughs (5.1809 ± 18.7990). Other factors like trip distance, additional cost (e.g. extra, tip, tolls), and hour of pick up are on the queue of the list.  

To get more distributed taxi services all over areas or boroughs, the Taxi and Limousine Commission (TLC) could:  
- make a better policy for better fare rates in other areas,  
- educate people & publish about the advantage of a legal taxi over an illegal taxi,  
- further study the social & geographical factors that might make this analysis more comprehensive & deep.  
  

## Project Context  
The majority of New Yorkers depend on public transportation or taxi services. Only 22% of Manhattan residents own a car, compared to an average of 91% of households across the United States owning at least one car. Taxi service in New York is the fourth largest transportation network in the United States.  

The system is regulated by the New York City Taxi and Limousine Commission (TLC), which oversees yellow taxis, charter taxis, commuter cars, transit vehicles, and certain limousines. Despite its large network, the current system does not serve the boroughs equally. Because of this, residents prefer illegal taxi services that have inconsistent access and fares.  
  
  
## Project Requirement  
1. What causes the yellow taxi service to only be concentrated in certain boroughs, causing an imbalance in demand and supply in other boroughs?   
2. TLC wants their yellow taxi services to be spread evenly throughout the city of New York so they can respond to existing demand. What should TLC do in the short term (6 months) to overcome this challenge?   
3. Finding meaningful information inside the given dataset!  
  
 
## Project Planning  
1. Exploratory Data Analysis (EDA)
  - Data Structure Check (shape, datatype, head, tail)
  - Data Quality Check (missing value, outlier, distribution)
  - Data Cleaning (missing value, outlier, inappropriate values, high cardinality)
  - Content Investigation (hypothesis testing, predictive power check through descriptive/visualization and analytics)
2. Data Preprocessing & Feature Engineering
3. Feature Selection
4. Models Training
5. Analyze Model
6. Dashboard Development (Tableau)
  
  
## Main Findings  
The logistic regression model & random forest are trained with RandomSearch & evaluated with KFold CV and to find the best parameters. From the logistic regression model, the coefficients that are the most influential could be obtained. In addition, from the random forest model, the feature importance could be obtained also. They are all agree features that are represented economic factors (e.g. fare rate, total amount of payment) are the most influential factors that drive the phenomena. Other factors like trip distance, additional cost (e.g. extra, tip, tolls), and hour of pick up are on the next queue of the list. This findings could be easily spotted with the dashboard built by using Tableau & the pivot table. The dashboard shows that mostly the non-Manhattan’s taxi services are majority drive for long distance, but only get less payment than the Manhattan’s taxi services.
  

## Other Meaninful Findings  
**Univariate Analysis**  
- VendorID mostly is coming from VeriFone (71%)
- RateCodeID mostly use Standard rate (96%)
- Store & Forward Flag mostly is not store & forward (~99%) the operation area is moslty in connected area to the server
- Two payment types mostly used are by CC (77%) & by cash (22%), this makes sense to avoid hassle
- The pickup & dropoff borough mostly is Manhattan (~91% & ~90% respectively)
- The operation area that pickup & dropoff are both in Manhattan is more than 87%
- Passenger_count mostly is 1 person
- Trip_distance mostly is in range 2-3 miles
- Fare_amount mostly is in range 9-12 buck
- Extra mostly is in range 0.5-1 buck
- Mta_tax is always 0.5 buck
- Tip_amount mostly in range +/-2 buck
- Tolls_amount is mostly 0
- Improvement_surcharge is always 0.3 buck
- Total_amount is in range 15-18 buck
- Congestion_surcharge is in range 2.5 buck
- Airport_fee is mostly 0
- Duration_hour is mostly in range 0.2 hour

**Bivariate Analysis**  
- Mostly yellow taxi(s) prefers to choose short distance trip (low payment, but very frequent) 
- There is no different in term of passenger count for both Manhattan & non-Manhattan borough
- The fare_rate & total_amount_rate are higher in the Manhattan borough
- The additional_cost is lower in Manhattan (an additional cost is the sum of all cost except from the fare amount)
- The operation in Manhattan borough is slightly decreasing in non-weekday(working day) from 88% to 86%
- The fare_rate in all payment_type categories is always higher in Manhattan

  
## Recommendations
To get more distributed taxi services all over areas or boroughs, the Taxi and Limousine Commission (TLC) could:  
- make a better policy for better fare rates in other areas
- educate people & publish about the advantage of a legal taxi over an illegal taxi,
- further study the social & geographical factors that might make this analysis more comprehensive & deep.

