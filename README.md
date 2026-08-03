# 🗺 Donald's Portfolio

Welcome to my data portfolio! Here, I document a selection of projects in data science, machine learning, and healthcare analytics.

## 📚 Table of Contents
- [Health Data & Machine Learning](#health-data--machine-learning)
- [Hypothesis Testing](#hypothesis-testing)
-[Visualizations](#visualizations)

# Health Data & Machine Learning

| Project Link | Tools | Description | Results |
|---|---|---|---|
| 🩺 **Predicting Type 2 Diabetes from Behavioral Risk Factors**<br>[-->Live app](https://diabetes-risk-app-bmtjnx8yhpebeuuqjdpynd.streamlit.app/) <br>[-->Repository](https://github.com/DonaldMAndrew/diabetes-risk-app) | Python, pandas, scikit-learn, SHAP, Streamlit | Random Forest classifier trained on CDC BRFSS 2014 survey data (117,141 respondents, 27 behavioral and health predictors).<br><br>Uses SHAP explainability to provide both global feature importance and local explanations for individual predictions.<br><br>Deployed as a [Streamlit application](https://diabetes-risk-app-bmtjnx8yhpebeuuqjdpynd.streamlit.app/) where users answer 25 survey questions, receive a predicted diabetes risk percentage, and view a personalized SHAP explanation showing which responses increased or decreased their predicted risk.<br><br>Class imbalance (~18% positive cases) was addressed using `class_weight="balanced"`. | Detects approximately [**73% of true diabetes cases** (recall ≈ 0.73)](https://github.com/DonaldMAndrew/diabetes-risk-app/blob/main/README.md#results), making it suitable as a screening-oriented model that prioritizes identifying potential cases over minimizing false positives.<br><br>[Most influential predictors include](https://github.com/DonaldMAndrew/diabetes-risk-app/blob/main/README.md#top-predictors) **BMI, general health, mobility equipment use, flu shot history, heart disease history, and age**. |


# Hypothesis Testing

| Project Link | Tools | Description | Results |
|---|---|---|---|
| 📋 **Patient Education & Knowledge Assessment (T2DM)**<br>[-->Repository](https://github.com/DonaldMAndrew/t2dm-education-impact/blob/main/README.md) | Python, pandas, numpy, scipy, matplotlib | Quasi-experimental pre-/post-test study measuring how a short pharmacist-led education session changes patients' knowledge of Type 2 Diabetes. <br><br> Built end-to-end: questionnaire design, education material, a synthetic 90-patient dataset, and a paired-samples t-test with assumption checks (Shapiro-Wilk normality, 1.5x IQR outlier check, Wilcoxon signed-rank as a non-parametric sensitivity check).<br><br> Adapted from a real hospital CKD study design; the disease focus, questionnaire and all data here are synthetic. | [Knowledge scores rose from 5.1/10 before the session to 8.5/10 after](https://github.com/DonaldMAndrew/t2dm-education-impact/blob/main/results.md#paired-t-test-results-synthetic-data-n90), a large, statistically significant improvement (t(89) = 17.76, p < 0.001, Cohen's d = 1.87), and the result held up under a backup test that doesn't assume normally distributed data.<br><br>



# Visualizations
| Project Link | Tools | Description | Results |
|---|---|---|---|
| 📊 [LyftMed Executive Intelligence Suite](https://github.com/donaldandrew/LyftMed-Executive-Intelligence-dashboard) | Power BI, DAX | A 7-page executive report covering revenue, partner risk, warehouse operations, lost sales, promotions, delivery/rider performance and geographic risk, built on a shared data model with 30+ custom DAX measures. |Found that promotions drive 56% of revenue but also over half of the company's total ₦601.22M revenue-at-risk, and traced ₦601M in risk down to two root levers: late delivery and stockouts. |
| 🧾 [CarePlus HMO Receivables Tracker](https://github.com/donaldandrew/CarePlus-HMO-Receivables-Tracker) |Excel (PivotTables, PivotCharts, slicers, SUMIFS) | Built an 11-month claims and collections tracker for an HMO client base, reconciling ₦186.14M invoiced against ₦140.86M collected. Practice dataset, fictional clients. | Found that the biggest client by value (51% of all invoicing) was also one of the best payers, while two mid-size clients were the real collections risk at only 21.6% and 36.1% paid. Also caught and corrected a mislabeled column in the source pivot before drawing conclusions from it. |


