### Problem Statement


The airbnb is a booming business in the hospitality industry right now . Many people are buying house or renting house to make them airbnbs and increase their income. 
The aim of this project is to build a regression machine learning model that can help in predicting the listing price of the airbnb and helping the owner understand the important features .

​
### Background
​
Airbnb stands for Air Bed and Breakfast. It was started in 2007 by roommates Joe Gebbia and Brian Chesky.
What started as a way to get some extra cash has become a multimillion company with a  net worth around $3.5billion at the end of 2020.
Airbnb connects travelers with Airbnb hosts who want to rent out their homes or other property. For guests, Airbnb gives affordable temporary housing options and sometimes fun activities. For hosts, Airbnb is a way to earn extra money

​
### Data Import and Cleaning
​
I got this dataset from Kaggle.com but it is a combination of different dataset from inside Airbnb.com.It is collection of some listing of houses in different city of United States.https://www.kaggle.com/kritikseth/us-airbnb-open-data

This dataset has one file- AB_US_2020.csv which has columns describing features such as host id, hostname, listing id, listing name, latitude and longitude of listing, the neighbourhood, price, room type, minimum number of nights, number of reviews, last review date, reviews per month, availability, host listings and city.

The dataset is made of 226030 rows and 17 features .
​
| Column | Type  | Description | 
| ----------- | ----------- | ----------- |
| id | integer | Airbnb's unique identifier for the listing |
|  name | object | Description of the airbnb |
| host_id | integer | Airbnb's unique identifier for the host/user  |
| host_name | object | Name of the host. Usually just the first name(s). |
| neighbourhood_group | object |The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. |
| neighbourhood | object |The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. |
| latitude | integer | Uses the World Geodetic System (WGS84) projection for latitude and longitude. |
|  longitude | integer | Uses the World Geodetic System (WGS84) projection for latitude and longitude. |
| room_type | object | Types of places to stay |
|  price | integer | daily price in local currency. Note, $ sign may be used despite locale |
| minimum_nights | integer | minimum number of night stay for the listing (calendar rules may be different)  |
| number_of_reviews | integer | The number of reviews the listing has |
| last_review | object | The date of the last/newest review |
| reviews_per_month | integer | The number of reviews the listing has per month |
| calculated_host_listings_count | integer | The number of listings the host has in the current scrape, in the city/region geography.|
|  availability_365 | integer | avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may be available because it has been booked by a guest or blocked by the host. |
|  City | object | the city in which the airbnb is located |
​
### Exploratory Data Analysis
​
 This part is divided into two sub part : the numerical and categorical features and The description for NLP(Nature Language Processing).

Analysed the distribution and relationship between features using visualization .

Analysed the description of the airbnb to understand how words are used 

​
​
### Modeling
​
Based on our problem statement to build a regression machine learning model that can help in predicting the listing price of the airbnb and helping the owner understand the important features, We used regression model that can help us with inference.

We built and compare  4  regression models using a linear regression as a baseline .
Linear regression,Decision tree , Random Forest  and XGboost models.
​
​
RESULTS:

|          Model           | Training RMSE | Testing RMSE |
|:------------------------:|:-------------:|:------------:|
|     Linear Regression    |    287.6      |     290.5    |
|       Decision Tree      |     5.1       |     320.6    |
|       Random Forest      |     129.6     |     234.2    |
|         XGBoost          |    211.13     |    236.07    |

|           Model          | Training score| Testing score|
|:------------------------:|:-------------:|:------------:|
|     Linear Regression    |     0.292     |     0.291    |
|       Decision Tree      |     0.99      |     0.17     |
|       Random Forest      |     0.94      |     0.57     |
|         XGBoost          |    0.69       |    0.58      |
​
​
### Conclusions and Recommendations
​
Looking at this score we are going to use the XGBOOST model because it has the lowest variance between the trainning and the test if even if it is overfit but it is 40% increase in accuray with the base line of the linear regression.
In terms of features importances , the Type of accommodation and location  are the important features necessary to predict the price. 
The city with the highest numbers of airbnbs are the touristic sities, entertairnment and vacation , considering having an airbnb there can be an extra source of income.
​
### Link to Jupyter Workbook:


​
### Source :
- [Background](#https://www.stratosjets.com/blog/airbnb-statistics/
