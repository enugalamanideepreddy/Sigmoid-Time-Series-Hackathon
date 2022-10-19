# sigmoid

We have imported new covid data which includes death cases too 'US_COVID_data_state_level.csv', city and city population data of US 'uszips.csv' and holiday data of US 'US Holiday Dates (2004-2021).csv' from trusted sources.

Data Preprocessing
  - Data Cleaning
    - Preprocessed data by removing duplicate cities from city data.
    - Preprocessed data to get unique zipcode for cities.
    - As we have imported city data from newlt imported 'uszips.csv' and from additional info ~warehouse_name~ column,  we have compared the city names and assigned the       new city names manually.
  
  - Performed data preprocessing
    - We have merged covid data with city, called it m.
    - we merged train data with warehouse data and called it x.
    - Then we've merged both m,x dataframe and called it z.
    - We have repeated the same for test data.
  
  - Feature Engineering
    - Using the extra imported data, we tried to create useful features (columns) for training the model.
    - The first feature we added is average total cases per each city by dividing tot_cases by number of cities of that state.
    - The second feature we added is the number of cases per city by using weighted average of population of city in that state.
    - Similarly we followed the same approach to calculate number of deaths per city and average total deaths per each city.
    - After that we tried to choose best feature for training from all the extra features added.
 
Model
  - Used Long short term memory model to forecast the demand of each warehouse Using 2 deep layers of 64,32 units and leaky relu activation function.
  - LSTM are type of recurrent neural network capable of learning order dependence in sequence prediction problems.


