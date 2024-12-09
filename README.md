# banglore_home_price_prediction

Project Description:
The Bengaluru House Price Prediction project involves building a machine learning model to predict the prices of houses in Bengaluru based on various factors such as location, size, amenities, and other features. This is achieved using a dataset of real estate properties in Bengaluru, and the project focuses on cleaning, preprocessing, and feature engineering to improve the accuracy of the predictions.

Data Preprocessing:
Loading the Dataset: The dataset is loaded from a CSV file (bengaluru_house_prices.csv), which contains information such as area type, availability, location, size, society, total square footage, number of bathrooms, balconies, and price.

Cleaning the Data:
Columns like area_type, society, balcony, and availability are dropped as they are not essential for the model.
Missing values are handled by removing rows where critical features like location, size, and bathrooms have null values.

Feature Engineering:
A new feature, bhk (Bedrooms, Hall, Kitchen), is created by extracting the number of bedrooms from the size column.
The total_sqft column is cleaned to handle cases with ranges (e.g., 2100 - 2850), where the average value is calculated.
A new feature, price per square foot, is created to normalize price against the area of the property.

Data Transformation:
Handling Categorical Data: The location column, which contains many unique values, is reduced by categorizing locations with fewer than 10 entries as "other."

Outlier Removal:
Using business logic, properties with a price per square foot that is too low for their size (e.g., less than 300 sqft per bedroom) are removed.
Outliers based on price per square foot are removed by considering the mean and standard deviation for each location to filter out extreme values.

Data Visualization:
Scatter plots are created to visualize the relationship between property size (square feet) and price for different numbers of bedrooms (BHKs), helping to identify trends and anomalies in the data.

Model Development:
After cleaning and transforming the data, this dataset is ready for model building. Various machine learning algorithms, such as linear regression, decision trees, or random forests, can be applied to predict house prices based on the cleaned features.
