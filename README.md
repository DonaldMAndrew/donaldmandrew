# 🗺 Donald's Portfolio

Welcome to my data portfolio! Here, I document a selection of projects in data science, machine learning, and healthcare analytics.

## 📚 Table of Contents
- [Health Data & Machine Learning](#health-data--machine-learning)
- - [Hypothesis Testing](#hypothesis-testing)

# Health Data & Machine Learning

| Project Link | Tools | Description | Results |
|---|---|---|---|
| 🩺 **Predicting Type 2 Diabetes from Behavioral Risk Factors**<br>[-->Live app](https://diabetes-risk-app-bmtjnx8yhpebeuuqjdpynd.streamlit.app/) <br>[-->Repository](https://github.com/DonaldMAndrew/diabetes-risk-app) | Python, pandas, scikit-learn, SHAP, Streamlit | Random Forest classifier trained on CDC BRFSS 2014 survey data (117,141 respondents, 27 behavioral and health predictors).<br><br>Uses SHAP explainability to provide both global feature importance and local explanations for individual predictions.<br><br>Deployed as a [Streamlit application](https://diabetes-risk-app-bmtjnx8yhpebeuuqjdpynd.streamlit.app/) where users answer 25 survey questions, receive a predicted diabetes risk percentage, and view a personalized SHAP explanation showing which responses increased or decreased their predicted risk.<br><br>Class imbalance (~18% positive cases) was addressed using `class_weight="balanced"`. | Detects approximately [**73% of true diabetes cases** (recall ≈ 0.73)](https://github.com/DonaldMAndrew/diabetes-risk-app/blob/main/README.md#results), making it suitable as a screening-oriented model that prioritizes identifying potential cases over minimizing false positives.<br><br>[Most influential predictors include](https://github.com/DonaldMAndrew/diabetes-risk-app/blob/main/README.md#top-predictors) **BMI, general health, mobility equipment use, flu shot history, heart disease history, and age**. |
