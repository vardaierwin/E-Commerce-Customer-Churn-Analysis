# E-Commerce Customer Churn Analysis

## Project Overview
This repository contains a Python-based data analysis project focused on exploring customer churn using a **public Kaggle dataset**: [E-commerce Customer Churn - Dataset](https://www.kaggle.com/datasets/absolutejoe/e-commerce-customer-churn-dataset) by Absolute Joe.

**Why this dataset?**  
I deliberately chose this relatively under-explored and less commonly used dataset (compared to more popular churn datasets like Telco or IBM samples) to challenge myself. Working with a less "pre-digested" dataset forced me to handle real-world-like cleaning issues, category inconsistencies, and derive meaningful insights without relying on widely available walkthroughs or kernels.

The dataset contains customer behavior and demographic features (e.g., tenure, preferred order categories, satisfaction score, distance from warehouse, cashback amount, complaints) with a binary **Churn** target. Through data cleaning and exploratory data analysis (EDA), the project uncovers patterns related to logistics friction, silent churn, tenure effects, and demographic segmentation.

This serves as a junior data analyst portfolio piece, demonstrating strong skills in:
- Data cleaning & preprocessing (Pandas)
- Exploratory Data Analysis & storytelling
- High-quality static visualizations (Matplotlib + Seaborn)

### Key Components
- **raw_data.csv**: Original downloaded file from Kaggle.
- **01_data_cleaning.ipynb**: Handles missing values (median imputation for skewed data), outlier removal (e.g., unrealistic warehouse distances >100 km), category standardization (e.g., "Mobile Phone" → "Mobile"), and feature engineering (derived labels like Satisfaction_Label, Address_status, Cashback_status).
- **02_eda.ipynb**: Full EDA with univariate, bivariate, and multivariate analysis. Includes 14 high-quality static PNG visualizations.
- **Visualizations (PNG folder or root)**: 14 exported images covering distributions, relationships, heatmaps, and business-oriented insights.

## Key Findings & Insights
(Explored from multiple angles: logistics, satisfaction, demographics, tenure)

1. **Logistics Friction (Distance Effect)**  
   - Local customers (0–10 km): lowest complaints (~26%) & churn (~14%).  
   - Extreme distance (30+ km): churn probability rises to ~20–33%, even among "Best" satisfaction customers.  
   → Delivery friction is a stronger churn driver than satisfaction alone.

2. **Silent Churn Phenomenon**  
   - 89.1% of non-complainers stayed, but 10.9% still churned silently.  
   - Among churned customers: Significant churn exists among 'Neutral' and even 'Good' ratings, proving that satisfaction scores alone don't predict loyalty.  
   → Many customers leave without raising formal complaints.

3. **Tenure & Loyalty Curve**  
   - Very new customers (1 month): high churn risk (~53%).  
   - Long-term (2+ years): near 0% churn.  
   → Early onboarding critical.

4. **Demographic Segmentation**  
   - Singles: prefer mobiles (43.5%), higher "Bad" satisfaction (20.8%).  
   - Married: prefer laptops & accessories (39.4%).  
   → Opportunity for personalized category promotions.

5. **Cashback as Recovery Tool**  
   - Low/medium cashback correlates with higher churn after complaints.  
   → Higher standardized recovery amounts could "buy back" loyalty.

## Visualizations (14 PNGs)
Examples include:

- Churn Probability vs. Distance 
- Churn Rate Heatmap (Satisfaction × Distance)
- Silent Churn Gap bar plot
- Preferred Category by Marital Status 
- Satisfaction Distribution among Churned (pie)

## Future Ideas

- Add basic churn prediction model (logistic regression / decision tree)
- Create interactive dashboard (Streamlit / Plotly)
- Compare with more popular churn datasets
