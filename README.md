# Disease Risk Predictor — XGBoost Upgraded

## Models

### Diabetes Model
- Algorithm: XGBoost with hyperparameter tuning
- AUC: 0.948
- Diabetic patient recall: 0.83
- CV Mean AUC: 0.943 — stable across 5 folds
- Threshold tuned to 0.3 for aggressive screening
- Most important feature: HbA1c level

### Heart Disease Model  
- Algorithm: XGBoost with hyperparameter tuning
- AUC: 0.904
- Heart disease recall: 0.93
- CV Mean AUC: 0.886
- Threshold tuned to 0.48 for balanced screening
- Most important feature: Chest pain type (cp)

## Why XGBoost
Upgraded from Random Forest to XGBoost with:
- GridSearchCV hyperparameter tuning
- Stratified K-Fold cross validation
- Custom threshold tuning for healthcare context
- Feature importance analysis

## Clinical Reasoning
- Diabetes threshold 0.3 — aggressive screening catches 83% of diabetics
- Heart disease threshold 0.48 — balanced approach catches 93% of patients
- HbA1c being top feature aligns with clinical diabetes diagnosis
- Chest pain type being top feature aligns with cardiology practice

## Why This Matters
Rural populations lack diagnostic access.
This tool acts as early screening — not diagnosis replacement.

## Libraries
Pandas, XGBoost, Scikit-learn, Numpy, Matplotlib
## Model Comparison

### Diabetes
| Model | Recall | Precision | AUC |
|-------|--------|-----------|-----|
| Random Forest | 0.72 | 0.51 | — |
| XGBoost | 0.83 | 0.41 | 0.948 |
| LightGBM | 0.72 | 0.53 | 0.944 |

### Heart Disease
| Model | Recall | Precision | AUC |
|-------|--------|-----------|-----|
| Random Forest | 0.89 | 0.85 | — |
| XGBoost | 0.93 | 0.66 | 0.904 |
| LightGBM | 0.87 | 0.74 | — |

Final model: XGBoost selected for both diseases
Reason: Highest recall — critical for healthcare screening
