# LR_Project
## Linear Regression Project Description
The purpose of this project is to design a linear regression model to predict the price of used cars. 

#### Data & Design
I set out to analyze used car listings from around big urban areas with prices between $5.000 and $50.000. Selenium crawler compiled listings on 11809 used cars with 19 features, and the price of the new version of each car was merged. I dropped variables that had more than half missing data. Some features could be further broken down into individual ones, for example, '2019 Honda Civic' was split into Year/Make/Model, and '6 Cyl Engine 2.5Lt' into 'Cylinders' and 'Engine Size'. Categorical non-numeric variables were converted into binary dummy variables. 

#### Algorithms
**Data Wrangling**:
Since some of the features were highly correlated, I used an iterative imputer to deal with some missing values for the 'Mileage' and 'Highway MPG' variables.
I used Levenshtein Distance to match the MSRP data to the used car listings data.
**Model Selection**:
The data was split into train/test subsets and scaled for testing of models with regularization.
LR, Lasso, Ridge, and Elastic Net models were trained and cross validated for different parameters. These were then compared with metrics like adj. R^2, MSE, and MEA. 
Shap values were calculated to see the influence of each individual feature on the performance of the model prediction. Oulier analisys was performed to detect and drop influentiat points with a high Cook's Distance. Polynomial Regression was performed, to best results. 

#### Tools
-   Selenium, requests & BeautifulSoup: Scrape and parse HTML 
-   sklearn.impute : Predictions to impute missing data
-   Fuzzywuzzy - Search matches between different sources
-   sklearn.linear_model : Create regression models
-   yellowbrick.regressor: Drop influential datapoints 
-   Shap: Visualization of influence of features in model.
#### Communication
The findings of this analysis are to be presented in a 5 minute slide presentation. 
