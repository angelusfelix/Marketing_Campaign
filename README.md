# Marketing Campaign
1. Problem Statement = Acceptance Rate is too small
2. Goal = To Increase Acceptance Rate 
3. Bussiness Metrics = Acceptance Rate
4. EDA process tell us about the dataset, dataset is a many feature describe their customer who response or not response their campaign
5. If we see the data, only 15% out of 2240 customer accept the campaign
6. I am Data Analyst will answer the callenge and get the revenue up

Download data = https://www.kaggle.com/datasets/rodsaldanha/arketing-campaign

# Bussiness Insight
1. Total Spending increase as Income increase
2. Wines and Meat are the customer who accept and not accept campaign favorite 
3. The rich customer (Income > USD700000) is prefer go shopping to store and browse through catalog
4. The customer who accepted the campaign is dominated by customer who vist the web 6-8 times.

# Bussiness Recommendation
1. In this customer account, please give recommendations by changing the web appearance to the products they buy most often to maintain the relationship between customers and our company
2. Provide good service when the customer comes to the store, modify the catalog and convince the customer that the quality of the product is the same as that in the catalog
3. Provide posters or advertisements through websites, e-catalogs, banners to increase the interest and experience of potential customers
4. Provide direct recommendations to high income customers who come directly to the store, or through the company's website.

# Prdict Model
1. Split Train Test = 80 Train, 20 Test
2. Transformation
  a. Product = Product[i] / Total_Product
  b. Purchase = Purchase[i] / Total_Purchase
  c. Age, dependents,NumWebVisitsMonth, Income, Year_Birth, Recency = MinMaxScalar
3. Feature Encoding
  a. Marital_status, Education = Label Encoding
  b. Segmentation = One Hot Encoding
4. Class Imbalance = Random Over Sampler
5. Algorithm: Recall Train and Recall Test : Condition
  a. Logistic Regression : 0.749 and 0.671 : Nice Model 
  b. K-Nearest Neighbor : 0.837 and 0.589 : Overfit
  c. Decision Tree : 1.00 and 0.219 : Overfit
  d. XGBoost : 0.769 and 0.712 : Nice Model, Best fit
  e. Adaboost :  0.766 and 0.726 : False Positive is too much
  f. SVM : 0.762 and 0.712 : Nice Model, Best fit 
  g. Random Forest Classifier : 1.00 and 0.219 : Overfit
  h. Naive Bayes : 0.80 and 0.794 : Best fit , False Positive is too much
XGBoost and SVM have same result, value Recall and Confussion Metrics. The difference between them only their feature importance.
6. Feature Importance, NumCatalogPurchases, NumDealPurchase, NumWebVisitsMonth, MntMeatProducts
