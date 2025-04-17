# App Success Prediction

This project predicts app success scores based on metadata and user reviews from the Google Play Store.

## 🧠 Objective
To build a machine learning model to predict app success, evaluate its performance, and create insights via Tableau dashboards.

## 📁 Data
- `apps.csv`: App metadata
- `reviews.csv`: User reviews

## 🎯 Target Variables
- **Success Score:** Installs * Rating
- **Log Success:** the log of success score

## Models Used
- Random Forest Regressor
- LightGBM Regressor
- XGBoost Regressor
- Linear Regression
- CatBoost

## 📊 Evaluation
- MAE for raw success score: 13.4M
- MAE for log-transformed: 10.7M when backtransformed. 
- Residual analysis and Mean Absolute Error were reviewed.

## ✅ Summary of Results 
- **Best Model:** XGBoost Regressor trained on apps_df with Log Success as target.
- Log transformation improved model performance due to heavy skew in the original success scores.
- Though the reviews dataset was helpful, it however introduced complexity without improving accuracy.
- Feature importance revealed key predictors like Reviews, Rating, Category and Genre.

## 🔍 Key Insights
- Apps targeted toward wider age groups(e.g Everyone, Everyone 10+) tend to attract more users
- The price contributes to the success of an app. Given most apps were free, it implies that free apps tend to perform better in terms of installs.    
- Sentiment Polarity, Review lenght and Word count have a minor positive correlation to the success matrices. Apps with positive sentiments and longer reviews tend to have higher success scores.
- Residuals indicate the log model generalizes better.

## 📈 Dashboard
See the Tableau Dashboard for app categories, app age, and success score distribution.
> Dashboard Link: _([Tableau Dashboard](https://public.tableau.com/app/profile/daisy.abbey/viz/GooglePlayStoreAppSuccessAnalysis/AppSuccessAnalysisDashboard?publish=yes))_

## 📚 How to Run
1. Clone the repo or download the notebook directory.
2. Ensure all dependencies are installed (see requirements.txt).
3. Run Notebook.ipynb step-by-step to follow through the entire pipeline.

```bash
pip install -r requirements.txt
```

## ✉ Contact 
For feedback or collaboration: [Daisy Abbey] | _([LinkedIn](https://www.linkedin.com/in/daisy-a-6394a1282))_

