# Predicting Corporate Default Risk Using Machine Learning

## A comparative study using Neural Networks (MLP) and XGBoost

This project builds machine learning models to predict the probability that a company will default using financial statement data.  
I used two different modeling approaches:  
- Neural Network (MLPClassifier)  
- XGBoost (Extreme Gradient Boosting)
  
Both models learn patterns from real company financial ratios—such as leverage, profitability, liquidity, and firm size—to estimate the chance that a company might fail.  
The goal is to compare how each model performs and understand which one is more suitable for credit-risk prediction.  

**Data Preparation**
Cleaned financial statement data
Created risk drivers (financial ratios commonly used in credit risk)
Standardized inputs for models
**Modeling**
I trained two machine learning models:
- Neural Network (MLPClassifier – scikit-learn)
 - Uses layers of connected “neurons”
 - Learns smooth nonlinear relationships
 - Good for modeling continuous and complex patterns

- XGBoost
 - Builds many mini decision trees
 - Very strong for tabular (row-and-column) data
 - Good at detecting thresholds and interactions (e.g., “high leverage + low cash → higher risk”)
   
**Evaluation**
I used 5-fold cross-validation at the firm level to avoid data leakage.  
Metrics include:  
- ROC-AUC (ranking ability)
- Accuracy
- Brier Score (probability quality)
- Log Loss
