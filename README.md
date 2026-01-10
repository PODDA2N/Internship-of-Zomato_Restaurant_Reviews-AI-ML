📊 Zomato Restaurant Review – Insights Report
🍽️ Zomato Restaurant Review Analysis & Prediction

📌 Project Overview

This project performs an end-to-end data analysis and machine learning workflow on the Zomato Restaurant Review dataset.
The objective is to clean and analyze restaurant and review data, validate assumptions using statistical tests, engineer meaningful features, and build machine learning models to predict restaurant cost categories and ratings.

📂 Dataset Description

The dataset consists of restaurant-level and review-level information.

Restaurant Information

Name – Restaurant name

Links – Zomato restaurant URL

Cost – Average cost for two people

Collections – Zomato collections the restaurant belongs to

Cuisines – Types of cuisines offered

Timings – Restaurant operating hours

Review Information

Restaurant – Restaurant name (review reference)

Reviewer – Reviewer identifier

Review – Customer review text

Rating – Customer rating

Metadata – Review metadata

Time – Review timestamp

Pictures – Review images availability

🔄 Project Workflow
1️⃣ Data Loading

Loaded dataset using Pandas

Verified shape, column names, and data types

Performed initial sanity checks

2️⃣ Dataset Information

Combination of numerical, categorical, text, and datetime features

Enables both structured analysis and NLP-based modeling

3️⃣ Understanding Variables

Cost and Rating act as target variables

Cuisines and Collections represent restaurant segmentation

Review captures customer sentiment

Time supports temporal analysis

4️⃣ Unique Value Analysis

Checked unique values per column to understand cardinality

Identified high-cardinality fields (Restaurant, Reviewer)

Confirmed categorical suitability for modeling (Rating, Cost_Category)

5️⃣ Data Preprocessing

Converted numerical columns (Cost, Rating) to numeric types

Handled missing and duplicate values

Normalized text data (lowercasing, trimming whitespace)

Parsed datetime fields from Time

6️⃣ Data Wrangling

Split and exploded multi-valued columns (Cuisines, Collections)

Standardized categorical values

Aggregated restaurant-level and review-level data where required

7️⃣ Data Visualization

Used Matplotlib and Seaborn for EDA:

Cost distribution histograms

Box plots of cost by cuisine and collection

Bar plots of average cost by cuisine

Correlation heatmap using engineered numerical features

8️⃣ Hypothesis Testing

Conducted statistical tests to validate assumptions:

One-Way ANOVA

Tested whether restaurant cost differs across cuisine types

Result: Statistically significant differences observed (p < 0.05)

T-Test / ANOVA

Compared costs across collection categories

9️⃣ Feature Engineering

Created new features to improve analysis and modeling:

Cuisine_Count

Collection_Count

Name_Length

Timings_Length

Cost_Category (Budget / Mid-range / Premium)

TF-IDF features extracted from review text

🔟 Machine Learning Model Implementation
Models Used:

Linear Regression – Cost prediction

Logistic Regression – Cost category / rating classification

Workflow:

Feature selection and encoding

Train-test split

Feature scaling

Model training using .fit()

Prediction using .predict()

Performance evaluation

1️⃣1️⃣ Model Prediction

Predicted cost and rating categories for unseen restaurants

Demonstrated model generalization and usability for business insights

📈 Model Evaluation Metrics

Regression: R² Score, MAE, RMSE

Classification: Accuracy, Precision, Recall, F1-Score

📌 Key Insights

Restaurants offering multiple cuisines generally have higher costs

Premium collections show significantly higher median pricing

Review sentiment contributes to rating prediction

Pricing varies significantly across cuisine categories

🧠 Business Impact

Enables data-driven restaurant segmentation

Supports pricing and recommendation strategies

Helps understand customer sentiment and preferences

Useful for restaurant owners and food-tech platforms

🛠️ Tools & Technologies

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

NLP (TF-IDF)

🚀 Future Enhancements

Advanced NLP models (Word2Vec, BERT)

Tree-based models (Random Forest, XGBoost)

Interactive dashboards (Power BI / Tableau)

Sentiment-based recommendation system
