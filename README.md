# Disease-Condition Detection from Drug Reviews

Predict a patient’s underlying medical condition directly from their free-text drug reviews.

## 1. Problem Statement

Given a review such as:

> “I’ve had nightly heartburn for months … omeprazole finally let me sleep.”

Our goal is to classify the condition (e.g. GERD) that the drug is treating.

This turns unstructured patient feedback into structured clinical insight.

## 2. Dataset

**UCI Machine-Learning Repository – Drug Reviews (V1)**

- 125,000+ reviews
- 2005 – 2020
- Fields: `drugName`, `condition`, `review`, `rating`, `date`, `sentiment`

## 3. Approach

- Exploratory Data Analysis
- Text cleaning & normalization  
  – lower-casing, punctuation stripping, stop-word removal, lemmatization
- Feature engineering  
  – TF-IDF (1–2 grams)
- Modelling  
  – Multinomial Naïve Bayes  
  – Logistic Regression  
  – (optional extensions: SVM, Random Forest, XGBoost)
- Evaluation  
  – Accuracy, precision, recall, F1, confusion matrix  
  – 5-fold cross-validation

## 4. Results (snapshot)

- **Logistic Regression**: ≈ 0.82 accuracy
- **Naïve Bayes**: ≈ 0.79 accuracy

Most frequent mis-classifications occur between conditions with overlapping symptom language (e.g. Anxiety vs Depression).

## 5. Repository Structure