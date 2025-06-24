# Files:
-company_info.csv
    - List of S&P 500 companies as of July 2022 and various metadata in tabular format
    - Contains information for over 500 companies
    - 4 attributes per company (4 columns)
        - Symbol: company symbol/brand
        - GICS sector: Global Industry Classification Standard sector that signifies which industry this company belongs to
        - Headquarters Location: location of company headquarter
        - Founded: year when company was first created (gives you a sense of company age)
- company_stock_details.csv
    - This file containing stock price, trade volume, news events and news sentiment for the companies listed in company_info.csv during the period Oct 2020-Jul 2022
    - 217811 samples in total
    - Total 18 features per date of stock exchange of a company (one row)
        - Date: date of exchange (basis for the time series data)
        - Close: final price at which the stock is traded just before the stock exchange officially closes for the day (this is the number you have to predict)
        - Volume: total shares traded during the day.
        - Symbol: company symbol/brand (common attribute with company_info.csv)
        - column 5 - 18: Different types of news volume regarding a company stock that may affect the price


# Additional Information:
- "Symbol" which denotes the company brand, is the common feature between the two datasets
- Missing values are there in the dataset
- Categorical, discrete and continuous attributes exist in the dataset
- The prediction tasks are regression tasks


# Prediction Task:
- Focus on predicting "Close" (closing price of the day)
- Given the stock information of at least the past 5 days of all companies, try to predict the closing price of one company on a particular day
    - all companies in training set and all companies in test set
    - some companies in training set and other companies only in test set
- Given the stock information of at least the past 5 days of one particular company, try to predict the closing price of that company on a particular day


# Task Expectation:
- Make sure that train and test data have minimum information leakage:
    - The days covered in your training data should have no overlap whatsoever with the days covering your test set
- If you exclude some features, you need to show proper visualization of why these samples have very low correlation with your prediction
- You are expected to explore both deep learning based time series modeling and traditional ML techniques
