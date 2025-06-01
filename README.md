# Predict the star rating associated with user reviews
[Kaggle Competition](https://www.kaggle.com/competitions/cs-506-spring-2025-technical-midterm)

![image](https://github.com/user-attachments/assets/5edd22a9-6e53-4354-b8c0-025a2f28dce9)


# Project Report

## Pre-processing (Experimented)
- Tried lemmatization, removing punctuation, and stop words, but it did not help in modeling

## Feature Engineering (Experimented)
- Created new columns `Sentiment`, `Subjectivity` from `Text` using `TextBlob`'s polarity and subjectivity function
- Created new column `text_length`
- Omitted all other features
- Performed `TF-IDF` vectorization for the above 3 columns
- No improvement observed

## Feature Engineering (Final)
- Created new column `Summary and Text` by concatenating the `Summary` and `Text` columns
- Performed `TF-IDF` vectorization for the above column
- Omitted all other features

## Model
- Sampled *10,000* data points from training set
- Ran trials with *8000* training points and *2000* validation points
- Tried `Random Forest`, `Decision Trees`, `SVM` with the above features
- Observed maximum of **54** val accuracy
- Obtained **59** val accuracy with `Logistic Regression`
- Observed **65.36** public accuracy in Kaggle
- Observed **65.55** final private accuracy in Kaggle
