# Smart Customer Clustering

This project focuses on customer segmentation using unsupervised machine learning. It analyzes customer data to identify patterns based on demographics, income, family structure, and purchase behavior. The goal is to group similar customers together so a business can better understand customer types, improve marketing strategies, and design personalized offers.

## Project Objective

The main aim of this project is to:

- segment customers into meaningful clusters
- identify high-value and low-value customer groups
- understand buying behavior and customer engagement patterns
- support marketing and sales decisions using data-driven insights

This is a classic example of unsupervised learning where the model groups customers without using predefined labels.

## Business Use Case

Retail businesses and e-commerce brands often need to understand:

- who are their loyal customers?
- who are the high-spending customers?
- which customers are inactive or low-engagement?
- which group should receive discounts or retention campaigns?

Using clustering, we can categorize customers into groups such as:

- premium/high-income loyal shoppers
- budget-conscious buyers
- occasional shoppers
- families with children and regular spending patterns
- inactive or low-engagement users

## Dataset

The dataset used in this project is stored in:

- `smartcart_customers.csv`

It contains customer information such as age, education, marital status, income, household details, purchase history, and response behavior.

### Key Features in the Dataset

- `ID`: unique customer identifier
- `Year_Birth`: customer's birth year
- `Education`: education level
- `Marital_Status`: marital status
- `Income`: annual income
- `Kidhome`: number of children at home
- `Teenhome`: number of teenagers at home
- `Dt_Customer`: date the customer joined
- `Recency`: number of days since last purchase
- `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`: spending by product category
- `NumDealsPurchases`: number of purchases via deals
- `NumWebPurchases`: number of purchases through website
- `NumCatalogPurchases`: purchases through catalog
- `NumStorePurchases`: purchases from store
- `NumWebVisitsMonth`: monthly website visits
- `Complain`: complaint indicator
- `Response`: response to offers or campaigns

## Data Preprocessing

Before clustering, the project performs several preprocessing steps:

- handling missing values in `Income`
- converting `Dt_Customer` to datetime format
- creating a derived feature: `Age`
- creating customer tenure using the date difference from the latest customer date
- calculating `Total_Spending` and `Total_Children`
- removing invalid or extreme values such as unrealistic age or income
- selecting relevant numerical features for clustering
- standardizing the dataset for better model performance

## Machine Learning Approach

This project uses an unsupervised clustering pipeline based on:

1. Data cleaning and feature engineering
2. Feature selection
3. Standardization
4. Dimensionality reduction using PCA
5. K-Means clustering
6. Elbow method to determine the optimal number of clusters
7. Cluster interpretation and visualization

### Clustering Model

The project applies the K-Means algorithm to segment customers based on key behavioral and demographic attributes. PCA is used to reduce dimensionality and make the clustering process more efficient and readable.

## Tools and Libraries

The project is implemented using Python and the following libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- Jupyter Notebook

## Project Files

- `README.md` – project documentation
- `smartcart_customers.csv` – raw customer dataset
- `smartcart.ipynb` – main clustering notebook

> Only the main dataset and clustering notebook are included in the project documentation.

## Workflow Summary

The notebook follows this flow:

1. Load the dataset
2. Explore the columns and missing values
3. Clean and engineer new features
4. Select the important attributes for segmentation
5. Standardize the feature values
6. Apply PCA for better cluster separation
7. Use the elbow method to choose cluster count
8. Train K-Means
9. Visualize customer groups and interpret the results

## Expected Outcome

The final output is a customer segmentation model that can help businesses identify different customer groups and tailor marketing campaigns accordingly. Examples of customer segments may include:

- loyal high-value customers
- price-sensitive buyers
- occasional shoppers
- family-oriented customers with higher purchase volume
- low-engagement or inactive users

## How to Run

Open the notebook in Jupyter and run all cells in order:

```bash
jupyter notebook
```

Then open:

- `smartcart.ipynb`

### Dependencies

Install required packages if needed:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## Conclusion

This project demonstrates how unsupervised learning can be used for real-world customer segmentation in retail and e-commerce. By grouping customers based on purchasing and demographic behavior, businesses can improve targeting, retention, promotions, and customer relationship management.

## Notes

This project is useful for:

- data analytics assignments
- machine learning portfolio projects
- customer segmentation studies
- business intelligence dashboard preparation

It can be extended further by adding:

- customer lifetime value analysis
- RFM analysis
- dashboard visualization using Power BI or Streamlit
- predictive modeling for churn or next-purchase prediction
