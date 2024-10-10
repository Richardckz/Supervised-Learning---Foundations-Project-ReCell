# Supervised-Learning---Foundations-Project-ReCell


Business Context
Buying and selling used phones and tablets used to be something that happened on a handful of online marketplace sites. But the used and refurbished device market has grown considerably over the past decade, and a new IDC (International Data Corporation) forecast predicts that the used phone market would be worth $52.7bn by 2023 with a compound annual growth rate (CAGR) of 13.6% from 2018 to 2023. This growth can be attributed to an uptick in demand for used phones and tablets that offer considerable savings compared with new models.

Refurbished and used devices continue to provide cost-effective alternatives to both consumers and businesses that are looking to save money when purchasing one. There are plenty of other benefits associated with the used device market. Used and refurbished devices can be sold with warranties and can also be insured with proof of purchase. Third-party vendors/platforms, such as Verizon, Amazon, etc., provide attractive offers to customers for refurbished devices. Maximizing the longevity of devices through second-hand trade also reduces their environmental impact and helps in recycling and reducing waste. The impact of the COVID-19 outbreak may further boost this segment as consumers cut back on discretionary spending and buy phones and tablets only for immediate needs.






# Data Description:

The data contains the different attributes of used/refurbished phones and tablets. The data was collected in the year 2021. The detailed data dictionary is given below.

brand_name: Name of manufacturing brand
os: OS on which the device runs
screen_size: Size of the screen in cm
4g: Whether 4G is available or not
5g: Whether 5G is available or not
main_camera_mp: Resolution of the rear camera in megapixels
selfie_camera_mp: Resolution of the front camera in megapixels
int_memory: Amount of internal memory (ROM) in GB
ram: Amount of RAM in GB
battery: Energy capacity of the device battery in mAh
weight: Weight of the device in grams
release_year: Year when the device model was released
days_used: Number of days the used/refurbished device has been used
normalized_new_price: Normalized price of a new device of the same model in euros
normalized_used_price: Normalized price of the used/refurbished device in euros







# MODEL PERFORMANCE
In this section, I provide an overview of the performance of the Linear Regression model that I built to predict the normalized price of used devices. The model was trained using the Ordinary Least Squares (OLS) method. Below are the key findings:

Model Overview
I created a Linear Regression model to predict how much used devices should cost. To build this model, I used a technique called Ordinary Least Squares (OLS). Think of OLS as a way of finding the best-fitting line through a bunch of points on a graph, where the goal is to make the line as close as possible to the actual data points..

Most Important Factors
The model I built uses the price of new devices to predict the price of used devices. The normalized_used_price (how much the used device costs) is strongly related to the normalized_new_price (how much the new device costs). This means if the new device is expensive, the used device will also be predicted to be more expensive.

Performance Summary
Here’s how well the model performed:

Metric	Train Data	Test Data
RMSE (Root Mean Squared Error)	0.375626	0.379049
MAE (Mean Absolute Error)	0.296987	0.294222
R-squared	0.695109	0.699165
Adj. R-squared	0.694857	0.698583
MAPE (Mean Absolute Percentage Error)	5.732845%	5.715602%
Here's what each metric means:

RMSE (Root Mean Squared Error): This tells us how far off the model’s predictions are from the actual prices, on average. For both the training data (used to build the model) and test data (new data), the numbers are around 0.38. Lower values are better.
MAE (Mean Absolute Error): This measures the average size of the mistakes the model makes, without considering if the mistakes are positive or negative. It’s around 0.30 for both sets of data. Lower values are better.
R-squared: This shows how well the model's predictions match the actual prices. An R-squared of about 0.70 means the model explains around 70% of the variation in prices. Higher values are better.
Adj. R-squared: This is similar to R-squared but adjusted for the number of variables in the model. It’s also about 0.70, showing that the model performs well and isn't overly complicated.
MAPE (Mean Absolute Percentage Error): This shows the average percentage of error in the predictions. For both data sets, it’s around 5.7%, meaning the model’s predictions are off by about 5.7% on average. Lower percentages are better.
Key Performance Metrics
The model demonstrates strong predictive performance, with similar metrics on both the training and test sets.
High R-squared values (around 0.695) indicate a good fit of the model to the data.
Low RMSE and MAE values suggest that the model makes accurate predictions.
MAPE values below 6% imply that the model is reliable for practical use.
