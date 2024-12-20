**Project TLC Taxi aims to achieve its goals using a dataset containing 22,699 rows and 18 columns:**\
A.	Predicting taxi fare using regression analysis.\
B.	Comparing Credit Card and Cash Payments using A/B test.\
C.	Predicting generous tippers using classification analysis.\
\
**A.	Predicting taxi fare using regression analysis.**\
•	A multiple linear regression model was built to predict taxi fares.\
•	A model uses five features—`VendorID`, `passenger_count`, `mean_distance`, `mean_duration`, and `rush_hour`—to predict fare_amount.\
•	The `mean_distance` feature had the greatest impact on the model's prediction.\
•	The model achieved 84% performance on the training data and 87% on the test data.\
•	The model's coefficient for `mean_distance` indicates that for every 3.57 miles traveled, the fare increases by $7.13, which averages to about $2.00 per mile.\
\
**B.	Comparing credit card and cash payments using A/B test.**\
•	Descriptive statistics compare average fares for each payment type, showing that credit card users tend to pay more than cash users. However, this could be due to random chance.\
•	To confirm the difference, a two-sample t-hypothesis test (independent t-test) with significance level 5% performed as part of the A/B test.\
•	There is a significant difference in the average fare amount between customers who use credit cards and those who use cash.\
•	The hypothesis test suggests that encouraging credit card payments could help increase revenue.\
\
**C.	Predicting generous tippers using classification analysis.**\
•	Tree-based models can predict whether a customer is a generous tipper (those tipping 20% or more).\
•	Descriptive statistics compare average tip for each payment type, showing that credit card users tend to tip more than cash users.\
•	Use data such as tipping history, pickup/dropoff times and locations, estimated fares, and payment methods to build models (random forest and gradient boosting).\
•	`VendorID`, `predicted_fare`, `mean_duration`, and `mean_distance` are the most important features. `VendorID` is the most predictive feature. This seems to indicate that one of the two vendors tends to attract more generous customers.\
•	Gradient boosting model is the champion, with F1 score test 73%, ~0.03 higher than the random forest.\
•	The model is nearly twice as likely to predict a false positive (predicting a generous tip when it's actually low) than a false negative (predicting no generous tip when it is actually generous). This indicates that type I errors are more common.\
