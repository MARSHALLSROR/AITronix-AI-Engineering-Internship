# 📰 BBC News Text Classification (LSTM vs TF-IDF)

This project implements and compares **deep learning** and **classical machine learning** approaches for multi-class text classification using the BBC News dataset.

It is part of my **AI / Deep Learning Internship Portfolio**, completed before moving to transformer-based models (BERT).

---

## 📌 Project Objective

Classify news articles into one of five categories:

- Business
- Entertainment
- Politics
- Sport
- Tech

The goal is to:
- Build a strong **baseline NLP pipeline**
- Compare **sequence models vs feature-based models**
- Establish reliable evaluation before introducing BERT

---

## 🧠 Models Implemented

### 1️⃣ Bi-LSTM (Deep Learning)
- Tokenization + Padding
- Embedding Layer
- Bidirectional LSTM
- Softmax output layer
- Early stopping to prevent overfitting

**Accuracy:** ~96%

---

### 2️⃣ TF-IDF + Linear SVM (Classical ML)
- TF-IDF vectorization (unigrams + bigrams)
- Linear Support Vector Classifier

**Accuracy:** ~98–99%

---

## 📊 Model Comparison

| Model | Accuracy | Strengths |
|------|---------|-----------|
| Bi-LSTM | ~96% | Captures word order & context |
| TF-IDF + SVM | ~99% | Fast, strong baseline, interpretable |

👉 Result: **TF-IDF + SVM outperformed Bi-LSTM on this dataset**, which is common for small/medium text corpora.

---

## 📁 Project Structure

0.3 BBC-classification/
│
├── notebooks/
│ └── bbc_news_classification.ipynb
│
├── models/
│ ├── bbc_bilstm_model.keras
│ ├── svm_tfidf_model.joblib
│ ├── tfidf_vectorizer.joblib
│ └── label_encoder.joblib
│
└── README.md


---

## 💾 Saved Artifacts

All trained components are saved for reproducibility:

- **Bi-LSTM model** (`.keras`)
- **SVM model** (`joblib`)
- **TF-IDF vectorizer**
- **Label encoder**

These allow:
- Reloading models without retraining
- Consistent inference pipelines

---

## 🔮 Next Steps

- Implement **BERT / Transformer-based classification**
- Compare:
  - Training time
  - Accuracy
  - Inference behavior
- Explore explainability (attention, SHAP)

---

## 🛠 Tech Stack

- Python
- TensorFlow / Keras
- scikit-learn
- spaCy
- NumPy / Pandas
- VS Code
- Kaggle
