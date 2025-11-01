# Retail Transaction Analysis and Recommendation System

This project was completed as part of the **Transaction-based Analytics & Recommendation Systems (ADA15)** course within the **Advanced Data Analytics in Business** study program.

### Dataset

The analysis is based on the [Retail Transaction Dataset](https://www.kaggle.com/datasets/bkcoban/retail-transaction-dataset) from Kaggle.
The dataset contains **transactional data** representing retail purchases, including:

* Transaction IDs
* Product names
* Quantities purchased

Although the data is **synthetic**, it preserves the structure of real-world retail transactions and allows the exploration of association-based recommendation methods.

### Data Preparation and Analysis

The dataset was cleaned and transformed into a **binary transaction matrix** (invoices × products).
Exploratory analysis was performed to examine product frequencies, distribution of basket sizes, and purchase patterns.
Association rules were then generated using the **Apriori algorithm**, with key metrics such as **support**, **confidence**, and **lift** computed to identify frequent itemsets.

### Recommendation Function

A custom **bidirectional recommendation function** (`recommend_products_bidirectional`) was implemented.
Unlike standard rule-based recommenders, it takes into account **both antecedents and consequents** of association rules, assigning weights based on match completeness and rule strength (lift × confidence).
The function outputs top-N product recommendations for a given basket.

### Results

* **Coverage:** 92.5% of unique products received at least one recommendation
* **Diversity (Gini–Simpson Index):** 91.55%
  These results indicate high model coverage and recommendation diversity, showing that the rule-based approach effectively captures product relationships within the dataset.
