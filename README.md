# 📰 Fake News Detection using NLP & Machine Learning

This project is designed to **understand and implement the core concepts of text analytics and machine learning** using a Fake News classification problem.  
The focus of this work is not just prediction, but learning how **raw text is processed, transformed, and modeled** using different machine learning techniques.

The system classifies news articles as **Fake** or **Real** using **NLP, vectorization, dimensionality reduction, and multiple classifiers**.

---

## 🎯 Learning Objectives

This project helps in understanding:

- **Regex-based text cleaning and parsing**
- **Text vectorization using TF-IDF**
- **Dimensionality reduction using Truncated SVD**
- **How different machine learning classifiers perform on text data**

---

## 📂 Dataset

Two datasets are used:

| File | Description |
|------|------------|
| `True.csv` | Real news articles |
| `Fake.csv` | Fake news articles |

Each file contains:
- `title`
- `text`
- `subject`
- `date`

Labels assigned:
- **1 → Real News**
- **0 → Fake News**

The datasets are merged into one training set.

---

## 🧩 Text Preprocessing (Regex)

The raw news text is cleaned using **Regular Expressions (Regex)**:

- Removal of punctuation  
- Removal of numbers  
- Removal of special characters  
- Conversion to lowercase  
- Removal of extra spaces  

This ensures the model learns from meaningful words only.

---

## 🔢 Feature Engineering

### 1. TF-IDF Vectorization  
The cleaned text is converted into numerical form using:

**TF-IDF (Term Frequency – Inverse Document Frequency)**

This represents how important a word is to a document relative to the entire dataset.

---

### 2. Truncated SVD  
TF-IDF produces very high-dimensional data.  
To make learning efficient, **Truncated SVD (Latent Semantic Analysis)** is applied to:

- Reduce feature dimensionality  
- Capture hidden semantic structure  
- Improve computational efficiency  

---

## 🤖 Machine Learning Models Used

The reduced text features are used to train multiple classifiers:

| Model |
|------|
| Logistic Regression |
| Linear Discriminant Analysis (LDA) |
| K-Nearest Neighbors (KNN) |
| Decision Tree Classifier |
| Gaussian Naive Bayes |

These models are trained and compared on the same data.

---

## 📊 Evaluation Method

The models are evaluated using:

**✔ Accuracy Score**

Accuracy measures how many predictions were correctly classified as Fake or Real.

---

## ⚙️ Workflow

1. Load Fake and Real news datasets  
2. Assign labels (Fake = 0, Real = 1)  
3. Merge datasets  
4. Clean text using Regex  
5. Convert text to TF-IDF vectors  
6. Apply Truncated SVD  
7. Train multiple ML classifiers  
8. Evaluate models using Accuracy  

---

## 🛠️ Technologies Used

- Python  
- Pandas & NumPy  
- Scikit-learn  
- NLTK  
- Regular Expressions (re)  

