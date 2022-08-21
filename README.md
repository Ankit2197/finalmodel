# TeamB_Model_Deployment
Predicting next 7-days Stock-price of Real-time data.
## Introduction
Trading is the platform where people invest their money to buy and sell shares of company to maximise their profit on investments. There are various technical indicators available in various trading site that helps indiviual to know about when to enter and exit from market. It will ne always better to know how the particular stock is going to perform in next 7-days as it will help individual in making better decisions. Also it will maximise the numbers of person who invests in stock as risk will be minimal. Thus the aim of our project is to deploy Machine Learning model that could predict the Closing stock price of real-time stock value of next 7-days by using machine learning techniques like Linear Regression and LSTM deep learning method.

## Dataset
We have used real-time data from yahoo finance to make model and prediction. Also we used S&P500, GDP,Employment rate, Production price index and fed funds dataset to see the dependency of economical indicators on stock price.

## Important Features
*Open:*-Its the open share price of stock in a particular day.
*High:*- Its the highest value of share recorded in a particular day.
*Low:*- Its the lowest value of share recorded in a particular day.
*Close:*-Its the closing share price in a particular day
*Volume:*- Its the number of bought and sold shares for a particular stock in a day.

#### Target Variable
Our Target variable is "Close", as we are specific to only interday investments.

#### Data Cleaning
For S&P500 dataset-As volume contains null value and volume means the number of shares bought or sold during the paricular period i.e. can't be calculated from given dataset. So removed the volume column. Since 33 rows of column Close/Last, High, Low is having 0.00 value. They belong to the date of christmas,new year,etc.. So, removed such missing rows.

#### Encoding and Scaling
We used One Hot Encoding technique to encode categorical variables to numerical feature. We used min_max scaler of standard scaler to scale data.

## Model Used:
This is non-stationary time-series dataset, so we used deep learning LSTM model and linear regression model. The idea is such that for a particular day the last 15 days will act as a input to observe the pattern and give the output as current day. So every 16th day is the output of its previous 15days input pattern. In this fashion the training and test data gets trained.

### Training and Testing dataset
Split dataset into 70 % for Training and 30% for testing.

**STEPS for web app development:**
**1.** Importing required Libraries and intialize the flask object.
**2.** We have created our web page using **HTML** and styling of web page using **CSS**.
**3.** The date has to be taken input in date format.
**4.** Now , we have to join our HTML and CSS page with web app using Flask **app.route('/')**.
**5.** Now we take all the Inputs.
**6.** After getting all the inputs finally predict the output using **app.route('/predict')**.

## Requirement:
![image](https://github.com/Ankit2197/finalmodel/blob/main/requirement.PNG)
to run the file:
pip install -r requirements
change the current working directory to where the files are present.
flask run

## Deploy Our Model Using Heroku Platform:
**User Interface**
![image](https://github.com/Ankit2197/finalmodel/blob/main/Screenshot%20(18).png)

**Future Scope:**
More analysis on economic indicators to see the impact on particular segment of market and stock price.

Intraday stock price prediction model should be made. 

Addition classification column ("%risk") to be made to see whether at a particular moment buying or selling share will be beneficial or not.

**Output:**

![image](https://github.com/Ankit2197/finalmodel/blob/main/Screenshot%20(17).png)

**Conclusion:**

With this project we can predict the next 7-days closing price of any stock.
The input date will take the last 15 days data fit in the trained model for prediction.
We have processed the LSTM model for 50 epochs to get the minimum loss value.
To deploy in heroku we need extra file as Procfile.
We have done the various EDA to see the insights of different dataset. Compared the GDP, Employment rate, PPI of different countries which can be seen through below links.

**Browse link:**
App link - # TeamB_Model_Deployment
