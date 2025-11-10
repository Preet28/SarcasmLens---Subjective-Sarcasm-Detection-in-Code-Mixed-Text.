# SarcasmLens – Subjective Sarcasm Detection in Code-Mixed Text

## Overview
SarcasmLens is a machine learning-based system designed to detect sarcasm in code-mixed (Hindi-English) social media text.  
This project focuses on identifying linguistic cues and stylistic markers that distinguish sarcastic expressions from literal ones in informal, multilingual environments.

It includes three key components:
1. Baseline System – Classical models using TF-IDF features.  
2. Dataset – Code-mixed Hindi-English text used for training and testing.  
3. Data - Web Scraping for Validation – Reddit scraping scripts for collecting real-world Hinglish posts to validate the trained models.

---

## Project Structure

---

## Baseline Model
The baseline models are implemented using classical machine learning with TF-IDF embeddings.  
Models trained:
- Random Forest  
- Logistic Regression  
- Linear SVM  
- RBF SVM  

### Model Design
- **Feature extraction:** TF-IDF with unigrams and bigrams (`max_features = 8000`)  
- **Text preprocessing:**
  - Lowercasing  
  - Removing URLs, mentions, and hashtags  
  - Keeping Hindi + English characters  
  - Normalizing whitespaces  
- **Evaluation metric:** Weighted F1-Score (to handle class imbalance)  
- **Best model:** Determined based on F1-score performance on the validation set.  

The best-performing model is stored as `best_baseline_model.pkl`.

---

## Dataset Information
The dataset comprises Hindi-English (Hinglish) tweets annotated for sarcasm.  
The data includes:
- Cleaned tweet text (`unique_tweets.csv`)  - Train/test
- Validation Test data (`test.csv`)  
- Duplicate removal and preprocessing scripts (`remove_duplicate_tweets.ipynb`)

### Preprocessing Steps
1. Removing duplicate entries.  
2. Cleaning noise (URLs, symbols, excessive punctuations).  
3. Labeling sarcastic vs. non-sarcastic text.

---

## Reddit Web Scraping for Validation
The folder `Data - web scraping for validation` includes code for collecting real-world code-mixed Hinglish content from Reddit.  
Subreddits used:
- r/IndianDankMemes  
- r/desiHumor  
- r/BollywoodMemes  


---
