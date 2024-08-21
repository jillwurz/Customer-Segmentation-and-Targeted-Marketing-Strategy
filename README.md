# Customer Segmentation and Targeted Marketing Strategy

## Project Overview
This project focuses on developing a customer segmentation model to enhance the marketing strategy of a company. The model uses a dataset of customers to group them into distinct segments based on their purchasing behavior, demographics, and other relevant features. The insights derived from this analysis can be used to create targeted marketing campaigns, optimize product pricing, and ultimately increase company profits.

## Dataset
The dataset used in this project contains various attributes related to customers, their purchases, and interactions with marketing campaigns.

### Attributes:

#### People
- **ID**: Customer's unique identifier
- **Year_Birth**: Customer's birth year
- **Education**: Customer's education level
- **Marital_Status**: Customer's marital status
- **Income**: Customer's yearly household income
- **Kidhome**: Number of children in the customer's household
- **Teenhome**: Number of teenagers in the customer's household
- **Dt_Customer**: Date of customer's enrollment with the company
- **Recency**: Number of days since the customer's last purchase
- **Complain**: 1 if the customer complained in the last 2 years, 0 otherwise

#### Products
- **MntWines**: Amount spent on wine in the last 2 years
- **MntFruits**: Amount spent on fruits in the last 2 years
- **MntMeatProducts**: Amount spent on meat in the last 2 years
- **MntFishProducts**: Amount spent on fish in the last 2 years
- **MntSweetProducts**: Amount spent on sweets in the last 2 years
- **MntGoldProds**: Amount spent on gold in the last 2 years

#### Promotion
- **NumDealsPurchases**: Number of purchases made with a discount
- **AcceptedCmp1**: 1 if the customer accepted the offer in the 1st campaign, 0 otherwise
- **AcceptedCmp2**: 1 if the customer accepted the offer in the 2nd campaign, 0 otherwise
- **AcceptedCmp3**: 1 if the customer accepted the offer in the 3rd campaign, 0 otherwise
- **AcceptedCmp4**: 1 if the customer accepted the offer in the 4th campaign, 0 otherwise
- **AcceptedCmp5**: 1 if the customer accepted the offer in the 5th campaign, 0 otherwise
- **Response**: 1 if the customer accepted the offer in the last campaign, 0 otherwise

#### Place
- **NumWebPurchases**: Number of purchases made through the company’s website
- **NumCatalogPurchases**: Number of purchases made using a catalog
- **NumStorePurchases**: Number of purchases made directly in stores
- **NumWebVisitsMonth**: Number of visits to the company’s website in the last month

## Project Objective
The main objective of this project is to create a model that segments customers to help develop a targeted marketing strategy aimed at increasing the company's profits.

### What is Customer Segmentation?
Customer segmentation is the process of dividing customers into groups that share similar characteristics. This can be done using demographic, geographic, psychographic, and behavioral data.

### Advantages of Customer Segmentation
- Determine appropriate product pricing
- Develop customized marketing campaigns

## Features Used in Analysis
- **Age**: Derived from the 'Year_Birth' attribute
- **Income**: From the 'Income' attribute
- **Partner**: Derived from the 'Marital_Status' attribute
- **Children**: Sum of 'Kidhome' and 'Teenhome'
- **Total Amount Spent**: Sum of 'MntWines', 'MntFruits', 'MntMeatProducts', 'MntFishProducts', 'MntSweetProducts', and 'MntGoldProds'
- **Total Purchases**: Sum of 'NumWebPurchases', 'NumCatalogPurchases', 'NumStorePurchases', and 'NumDealsPurchases'
- **Total Accepted Campaigns**: Sum of 'AcceptedCmp1', 'AcceptedCmp2', 'AcceptedCmp3', 'AcceptedCmp4', 'AcceptedCmp5', and 'Response'

## Libraries Used
- **Pandas**: For data manipulation and analysis
- **NumPy**: For numerical computations
- **Matplotlib & Seaborn**: For data visualization
- **Scikit-learn**: For preprocessing and machine learning
- **Yellowbrick**: For visualizing the performance of machine learning models
- **Plotly**: For interactive visualizations

## Data Preprocessing
1. **Handling Missing Values**: 
   - The 'Income' column had missing values which were filled using the mean income.

2. **Feature Engineering**:
   - Converted 'Year_Birth' to 'Age'.
   - Created a binary 'Partner' feature from 'Marital_Status'.

3. **Data Cleaning**:
   - Dropped irrelevant columns for this analysis.

## Exploratory Data Analysis (EDA)
Performed exploratory data analysis to understand the distribution of features, identify patterns, and prepare the data for modeling.

## Model Building
The model was built using the KMeans clustering algorithm to segment customers into different groups. The number of clusters was determined using the Elbow Method.

## Results
The clustering model successfully grouped customers into distinct segments. These segments can be used to tailor marketing strategies, optimize product offerings, and improve customer retention.
