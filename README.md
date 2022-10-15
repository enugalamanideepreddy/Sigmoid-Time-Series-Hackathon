# sigmoid

We have imported new covid data 'US_COVID_data_state_level.csv', population data of US 'uszips.csv' and holiday data of US 'US Holiday Dates (2004-2021).csv' from trusted sources.

Performed data cleaning
  >> Removed duplicate cities from city data
  >> Removed one of the cities with same zip code
  
Performed data preprocessing
  >> merged covid data with city data set and we call it m
  >> we merged train data with warehouse data and called it x
  >> then merged both m,x dataframe and called z
  >> repeated for test data the same
  
Feature Engineering
  >> make column avg total cases based on number of cities in each state and also using weighted average on population.
  >> repeated above with total deaths
 
Model
  >>Used Long short term memory model to forecast the demand of each warehouse Using 3 deep layers with 128,64 and 32 units respectively.


