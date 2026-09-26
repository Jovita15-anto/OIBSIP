# 📧 Email/SMS Spam Detection using Machine Learning

## 📌 Project Overview

This project builds a Natural Language Processing (NLP) based machine learning
system to classify SMS messages as either **Spam** or **Ham (legitimate)**.

The project uses text preprocessing, TF-IDF feature extraction, and two
machine learning classification algorithms:

- Multinomial Naive Bayes
- Logistic Regression

The models are evaluated using accuracy, precision, recall, F1-score,
classification reports, and confusion matrices.

---

## 🎯 Objective

The objective of this project is to develop a machine learning classifier
that can automatically distinguish between spam and legitimate SMS messages.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- WordCloud
- Jupyter Notebook

---

## 📂 Dataset

The project uses the **SMS Spam Collection** dataset.

The dataset contains:

- **5,572 messages**
- **4,825 Ham messages**
- **747 Spam messages**

### Class Distribution

| Class | Count | Percentage |
|---|---:|---:|
| Ham | 4,825 | 86.59% |
| Spam | 747 | 13.41% |

The dataset is therefore imbalanced, with Ham messages representing the
majority class.

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Class Distribution Analysis
   ↓
Text Preprocessing
   ↓
Lowercase Conversion
   ↓
Punctuation Removal
   ↓
Stopword Removal
   ↓
TF-IDF Feature Extraction
   ↓
Train/Test Split
   ↓
 ┌──────────────────────┐
 │                      │
Naive Bayes      Logistic Regression
 │                      │
 └──────────┬───────────┘
            ↓
       Model Evaluation
            ↓
 Accuracy / Precision / Recall / F1
            ↓
       Confusion Matrix
            ↓
      Model Comparison

```
## 🧹 Data Preprocessing

The SMS messages were processed before training the machine learning models.

### 1. Lowercase Conversion

All messages were converted to lowercase to maintain consistency.

Example:

```
FREE Entry  ->  free entry
```

### 2. Punctuation and Special Character Removal

Punctuation and special characters were removed from the messages.

### 3. Stopword Removal
Common English stopwords were removed using scikit-learn's
ENGLISH_STOP_WORDS.

Examples include:
```
the, is, a, an, in, to, of, and
```
Informal SMS terms such as u, wif, lar, and oni were retained
## 🔢 TF-IDF Feature Extraction

TF-IDF stands for **Term Frequency-Inverse Document Frequency**.

It converts text data into numerical features that machine learning models
can understand.

TF-IDF gives higher importance to words that are important within a message
but less common across the entire collection of messages.

The TF-IDF transformation produced a matrix with:

- **5,572** messages
- **9,174** features

```
TF-IDF Matrix Shape: (5572, 9174)
```

## ✂️ Train/Test Split

The dataset was divided into training and testing sets using an 80/20 split.

The `stratify` parameter was used to maintain a similar Ham/Spam class
distribution in both datasets.

### Training Data

- Samples: **4,457**
- Features: **9,174**

### Testing Data

- Samples: **1,115**
- Features: **9,174**

```
Training data: (4457, 9174)
Testing data:  (1115, 9174)
```

## 🤖 Machine Learning Models

Two machine learning classification algorithms were trained and evaluated
for spam detection:

1. **Multinomial Naive Bayes**
2. **Logistic Regression**

Both models were trained using the TF-IDF features generated from the
preprocessed SMS messages.

### 1. Multinomial Naive Bayes

Multinomial Naive Bayes was used as the first classifier because it is
well suited for text classification problems.

#### Performance

| Metric | Score |
|---|---:|
| Accuracy | 96.23% |
| Precision | 100.00% |
| Recall | 71.81% |
| F1 Score | 83.59% |

The confusion matrix showed that the model correctly classified 966 Ham
messages and 107 Spam messages.

### 2. Logistic Regression

Logistic Regression was used as the second classifier to compare its
performance with Multinomial Naive Bayes.

#### Performance

| Metric | Score |
|---|---:|
| Accuracy | 94.71% |
| Precision | 98.91% |
| Recall | 61.07% |
| F1 Score | 75.52% |

The confusion matrix showed that the model correctly classified 965 Ham
messages and 91 Spam messages.

## 📊 Model Comparison

The performance of both classification models was compared using accuracy,
precision, recall, and F1-score.

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---:|---:|---:|---:|
| Multinomial Naive Bayes | 96.23% | 100.00% | 71.81% | 83.59% |
| Logistic Regression | 94.71% | 98.91% | 61.07% | 75.52% |

Based on the test-set results, Multinomial Naive Bayes achieved higher
accuracy, precision, recall, and F1-score than Logistic Regression.

## 📌 Why Recall is Important for Spam Detection

Recall measures how many of the actual spam messages are correctly identified
by the model.

A **false negative** occurs when an actual spam message is incorrectly
classified as a Ham message.

In spam detection, false negatives are important because a spam message that
is classified as Ham may reach the user's inbox.

Therefore, a higher recall helps the model detect a larger proportion of
actual spam messages.

In this project:

- Multinomial Naive Bayes Recall: **71.81%**
- Logistic Regression Recall: **61.07%**

Multinomial Naive Bayes detected a larger proportion of the actual spam
messages in the test dataset.

## ☁️ WordCloud Visualization

WordCloud visualizations were used as a bonus analysis to identify commonly
occurring words in Spam and Ham messages.

Two separate WordClouds were generated:

- Spam messages
- Ham messages

These visualizations provide a quick visual representation of frequently
occurring words in each class.

### Spam WordCloud

The Spam WordCloud highlights commonly occurring words found in spam
messages.

### Ham WordCloud

The Ham WordCloud highlights commonly occurring words found in legitimate
messages.

## 📈 Evaluation Metrics

The models were evaluated using four important classification metrics:

### Accuracy

Accuracy measures the overall percentage of correctly classified messages.

### Precision

Precision measures how many of the messages predicted as spam were actually
spam.

### Recall

Recall measures how many of the actual spam messages were correctly detected.

### F1 Score

F1-score is the harmonic mean of precision and recall. It provides a combined
measure of both metrics.

### Confusion Matrix

A confusion matrix shows the number of correctly and incorrectly classified
messages, including:

- True Positive (TP)
- True Negative (TN)
- False Positive (FP)
- False Negative (FN)

## 📝 Conclusion

This project demonstrates how Natural Language Processing and machine
learning can be used to automatically classify SMS messages as Spam or Ham.

The project included data cleaning, text preprocessing, TF-IDF feature
extraction, model training, and model evaluation.

Two classification models were trained:

- Multinomial Naive Bayes
- Logistic Regression

Based on the test-set results, Multinomial Naive Bayes achieved higher
accuracy, precision, recall, and F1-score than Logistic Regression.

The project demonstrates a complete NLP-based machine learning workflow for
text classification.

## 👩‍💻 Author

**Anto Jovita**

B.Tech – Artificial Intelligence & Data Science
