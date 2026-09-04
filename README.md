# Credit Risk Scoring Model

## Objective
Predict the probability that a client will default on a loan (bad payer) 
using the German Credit Data dataset, to support credit lending decisions.

## Methodology
- Logistic regression with scikit-learn
- Preprocessing: categorical feature encoding (dummy encoding), 
  numerical feature scaling
- Stratified train/test split (80/20)

## Results
- ROC-AUC: 0.83
- Accuracy: 0.80
- Recall for "bad payer" class: 0.58

## Business Insight
The model performs well at identifying good payers, but has room for 
improvement in detecting defaulters (recall: 0.58), which represents 
the costliest error for a financial institution. This opens the door 
to adjusting the model with class_weight='balanced' or exploring a 
different decision threshold than the default 0.5.

## Next Steps
- Test class_weight='balanced'
- Compare against Random Forest / XGBoost
- Adjust the decision threshold based on business cost
