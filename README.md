# Disease Risk Predictor

## What it does
Predicts diabetes and heart disease risk based on patient 
health parameters using Machine Learning.

## Models
- Diabetes — 94% accuracy, catches 72% of diabetic patients
- Heart Disease — 85% accuracy, catches 89% of heart disease patients

## How it works
- Random Forest Classifier for both diseases
- Handled class imbalance using class_weight='balanced'
- Full input validation and edge case handling
- Returns risk probability not just binary prediction

## Why this matters
Rural populations lack access to diagnostic facilities.
This tool acts as an early risk screening system.

## Dataset
- Diabetes: Kaggle diabetes prediction dataset
- Heart Disease: UCI Heart Disease dataset

## Libraries
Pandas, Scikit-learn, Numpy

## Example Output
predict_diabetes('Male', 60, 1, 1, 'current', 35.0, 8.5)
→ High diabetes risk. Probability: 87%
