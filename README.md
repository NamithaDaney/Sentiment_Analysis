# Sentiment Analysis using NLP
This project uses Natural Language Processing (NLP) and Machine Learning to classify text comments into different emotions.

The project classifies comments into:
1. Anger
2. Fear
3. Joy
   
This project demonstrates an end-to-end NLP text classification workflow, starting from raw text preprocessing and TF-IDF feature extraction to machine learning model comparison, evaluation, model serialization, and prediction on unseen text.

## Project Workflow

The project follows a simple process: preprocess the text → convert it into TF-IDF features → train and evaluate ML models → predict emotions.

### Text Preprocessing

Text is cleaned by lowercasing, removing unnecessary characters and stopwords, tokenizing, and handling missing values.

### Feature Extraction

TF-IDF converts the cleaned text into numerical features using unigrams and bigrams, with up to 5,000 features.

## Machine Learning Models

Two models are trained and compared:

1. Multinomial Naive Bayes: A commonly used algorithm for text classification.

2. Support Vector Machine (SVM): A Linear SVM is used because it works well with high-dimensional text features such as TF-IDF.

The model with better evaluation performance is selected as the final model.

## Saved Model Files

The trained model and TF-IDF vectorizer are saved using Joblib.

best_emotion_model_SVM_Linear.joblib
tfidf_vectorizer.joblib

The vectorizer is saved along with the model so that new text can be transformed in the same way as the training data.

