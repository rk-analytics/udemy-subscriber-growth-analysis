# **Understanding and Predicting Udemy Course Subscriber Growth**

## 📌 **Project Overview**

This project analyzes and models Udemy course subscriber growth using pre-launch course metadata, pricing information, and temporal features. The goal is to identify the key drivers of course popularity and evaluate how effectively machine learning models can predict subscriber growth before or shortly after course publication.
The analysis emphasizes interpretability and business relevance, positioning predictive modeling as a decision-support tool rather than a precise forecasting system.

## 📊 **Dataset**

The dataset consists of historical Udemy course metadata, including pricing, publication timelines, and course structure features. Only attributes available prior to or at the time of course publication were used to avoid post-enrollment data leakage.

### Key Features:
- Course pricing and discount status
- Number of published lectures and practice tests
- Course age and publication timing
- Course creation-to-publication duration
- Subscriber count (log-transformed target variable)

## 🔍 **Exploratory Data Analysis**

Exploratory analysis was conducted to understand the distribution of features and their relationships with subscriber growth. 
Key insights include:
- Course age is the strongest driver of subscriber accumulation.
- Courses with more published lectures tend to attract more subscribers.
- Discounted courses achieve higher enrollment volumes than non-discounted courses.
- Free courses generally attract more subscribers, though monetization was not evaluated.
These insights guided feature selection and model choice.

## 🤖 **Modeling Approach**

Multiple regression models were trained and evaluated to predict the log-transformed number of subscribers:
- Linear Regression (baseline)
- Ridge Regression
- Lasso Regression
- Random Forest Regression
Model performance was evaluated using R² and RMSE metrics. While linear and regularized models showed similar performance, Random Forest Regression achieved the best overall results by capturing non-linear relationships among features.

## 📈 **Model Performance & Interpretation**

The Random Forest model achieved the highest predictive performance among the evaluated approaches. While overall predictive accuracy is moderate, the model is better suited for identifying the relative drivers of subscriber growth rather than producing precise point predictions.
Feature importance analysis highlights the dominant role of:
1. Course age
2. Number of published lectures
3. Time taken to publish
4. Pricing and discount strategy

## 💡 **Business Recommendations**

#### For Course Creators:
- Invest in comprehensive course content with sufficient lecture depth.
- Maintain and update courses over time to sustain relevance.
- Leverage Udemy discount cycles to improve visibility and reach.

#### For Platform Strategy:
- Promote older, high-quality courses during major sales events.
- Highlight content depth and course structure in recommendations.
- Use discount-based targeting to drive subscriber acquisition.

## ⚠️ **Limitations**

- Revenue, completion rates, and learner engagement metrics were not available.
- Instructor reputation and course topic granularity were not included.
- Subscriber growth dynamics over time were not explicitly modeled.

## 🚀 **Future Improvements**

- Incorporate revenue, completion rates, and review sentiment analysis.
- Apply time-series or cohort-based modeling to capture subscriber growth dynamics.
- Experiment with advanced ensemble models such as XGBoost or LightGBM.
- Perform systematic hyperparameter tuning.

## 🛠️ **Tools & Technologies**

- Python
- Excel
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

## ✅ **Key Takeaway**

Subscriber growth on Udemy is driven primarily by course longevity, content depth, and pricing strategy. Predictive models are most effective as tools for insight and decision support rather than exact subscriber forecasting.







