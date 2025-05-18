# 📰 News Article Classification Project

## 📌 Project Overview
This project aims to build a machine learning model capable of classifying news articles into predefined categories (e.g., **politics**, **entertainment**, **wellness**) using textual data from headlines and descriptions. With effective preprocessing and feature extraction, the model is designed to achieve high accuracy and reliability in news classification.

## 🚀 Problem Statement
The objective is to develop a classification model that can automatically categorize news articles into different categories. This is achieved by training a model with labeled news articles, allowing it to predict the category (e.g., **Sports**, **Politics**, **Technology**) for any given article.

## 📂 Dataset
- **Source**: `news.csv` containing 50,000 articles
- **Fields Used**:
  - `headline`
  - `short_description`
  - `category`
- **Data Preparation**:
  - Combined `headline` and `short_description` into a new column `text`.
  - Focused on the top 7 categories to reduce label noise.

## 🔎 Data Exploration
- Visualized the distribution of articles across categories.
- Extracted top keywords per category using word frequencies.

## 🔄 Data Preprocessing
- Converted all text to lowercase.
- Removed URLs, HTML tags, punctuation, and stopwords using `nltk`.
- Applied word tokenization and whitespace cleanup.
- Stored the preprocessed content in a new column `clean_text`.

## 🛠️ Feature Engineering
- **Bag of Words (BoW):** Used `CountVectorizer` with 5,000 most frequent words.
- **TF-IDF:** Applied `TfidfVectorizer` (up to bigrams, 8,000 features).
- **Word2Vec:** Created 100-dimensional vectors using Gensim's Word2Vec.

## 🤖 Model Development & Evaluation
| Model               | 🎯 Accuracy | 💡 Notes                                      |
|----------------------|-------------|--------------------------------------------|
| **Logistic Regression** | 83.6%       | Best performer; robust with tuning (C, solver) |
| **Support Vector Machine** | 83.7%       | Strong generalization and comparable to LR    |
| **Naive Bayes**        | 82.4%       | Fast, simple, effective with TF-IDF           |

## 🔀 Ensemble Learning
- A **Voting Classifier** combining Logistic Regression, SVM, and Naive Bayes.
- **Cross-Validation Accuracy:** 83.8%, slightly better than individual models.

## 📊 Visualization
- Displayed category distribution and keyword frequencies.
- Plotted confusion matrices for each model to understand class predictions.

## 💡 Insights
1. Preprocessing and TF-IDF were crucial for boosting model accuracy.
2. Logistic Regression proved to be interpretable and highly effective.
3. Ensemble learning with multiple models enhanced stability and accuracy.

## 🔭 Future Work
- Experiment with BERT-based models for enhanced context understanding.
- Extend categories and add multilingual support.
- Integrate real-time classification for news streaming.

## 🎬 Video Explanation
[▶️ Video Walkthrough](https://drive.google.com/file/d/10GjSjZYA67LIcRuqYD9slTI1K-Z9Rc2l/view?usp=sharing)

---

Feel free to contribute to this project or raise issues for improvements.

### 👨‍💻 Author
**P Rohith Raveendran**
