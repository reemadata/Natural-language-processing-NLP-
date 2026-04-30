# Arabic Sentiment Analysis using Machine Learning

## 📌 Project Overview

This project focuses on building a machine learning model for **Arabic sentiment analysis**, where text is classified into **positive (pos)** or **negative (neg)** sentiments.

The project implements a complete text mining pipeline including preprocessing, feature engineering, model training, and evaluation.

---

## 📊 Dataset

* Source: Kaggle – Arabic Sentiment Texts
* Total Samples: 338,721
* Classes:

  * Positive (pos)
  * Negative (neg)

The dataset is relatively balanced, which helps ensure unbiased model performance.

---

## 🧹 Data Preprocessing

The following preprocessing steps were applied:

* Removal of URLs and mentions
* Removal of hashtags symbols (#)
* Arabic text normalization (e.g., إ → ا, ى → ي)
* Removal of diacritics
* Removal of special characters and numbers

---

## 🔧 Feature Engineering

Text data was transformed into numerical features using:

* **TF-IDF Vectorization**
* Maximum features: 9000
* N-gram range: (1,2) → Unigrams + Bigrams

This helps capture both individual words and contextual phrases.

---

## 🤖 Models Used

### 1. Logistic Regression

* class_weight = balanced
* max_iter = 200

### 2. Naive Bayes (MultinomialNB)

---

## 📈 Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

---

## 📊 Results

| Model               | Accuracy |
| ------------------- | -------- |
| Logistic Regression | 0.88     |
| Naive Bayes         | 0.85     |

**Logistic Regression outperformed Naive Bayes** due to its ability to model feature relationships.

---

## 🔍 Analysis

* TF-IDF with n-grams improved contextual understanding
* Logistic Regression handled feature interactions better than Naive Bayes
* Some errors occurred due to sarcasm, mixed sentiment, and dialect variations

---

## ⚠️ Limitations

* Difficulty handling sarcasm and implicit sentiment
* No deep learning models were used
* Arabic dialect variability

---

## 🚀 Future Work

* Use deep learning models (LSTM, BERT)
* Apply word embeddings (Word2Vec, FastText)
* Improve handling of dialects and sarcasm
* Use cross-validation for more robust evaluation

---

## 🛠️ Technologies Used

* Python
* Pandas
* Scikit-learn
* Matplotlib

---

## 📁 Project Structure

```
├── data/
├── NLP FINEL project.ipynb
├── README.md
```

---

## 📌 Notes

* Stratified train-test split was used to maintain class balance
* TF-IDF handles tokenization internally
* Class weights were used as a precaution for potential imbalance

