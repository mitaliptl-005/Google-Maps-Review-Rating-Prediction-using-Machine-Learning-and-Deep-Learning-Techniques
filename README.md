# Google Maps Review Rating Prediction using Machine Learning and Deep Learning

## Project Overview

This project predicts Google Maps review ratings (1–5 stars) using the textual content of customer reviews. The problem is formulated as a multi-class text classification task using Natural Language Processing (NLP), Machine Learning, and Deep Learning techniques.

The project compares traditional machine learning models such as Logistic Regression, Support Vector Machines (SVM), and Naive Bayes with advanced deep learning models including RNN, GRU, LSTM, and BERT.

---

## Objectives

- Predict customer review ratings from review text.
- Compare machine learning and deep learning approaches.
- Evaluate different text representation techniques.
- Perform topic modeling on positive and negative reviews.
- Identify the best-performing model for rating prediction.

---

## Dataset

The dataset contains approximately 288,000 Google Maps customer reviews.

### Features

| Feature | Description |
|----------|-------------|
| Review Text | Customer review text |
| Rating | Rating score (1–5) |


### Challenges

- Class imbalance across rating categories.
- Short reviews with limited context.
- Semantic complexity of natural language.
- Difficulty distinguishing between neighboring ratings.

---

## Text Preprocessing

The following preprocessing techniques were applied:

- Lowercasing
- Contraction expansion
- Punctuation removal
- Tokenization
- Stopword removal
- Lemmatization

Lemmatization was selected over stemming because it preserves semantic meaning more effectively.

---

## Feature Representation Techniques

### Bag of Words (BoW)

Represents documents using word frequencies.

### Binary Bag of Words

Represents word presence or absence.

### TF-IDF

Implemented using:

- Unigrams
- Bigrams
- Trigrams
- TF-IDF (1,2) (Unigrams + Bigrams)

### Word2Vec

Dense vector embeddings that capture semantic relationships between words.

## Machine Learning Models

### Logistic Regression

| Feature Representation | Test Accuracy |
|------------------------|---------------|
| TF-IDF (1,2) | 66.27% |

### Support Vector Machine (SVM)

| Feature Representation | Test Accuracy |
|------------------------|---------------|
| TF-IDF (1,2) | 64.82% |

### Naive Bayes

| Feature Representation | Test Accuracy |
|------------------------|---------------|
| BoW | 62.19% |

## Deep Learning Models

### Recurrent Neural Network (RNN)

- Word2Vec embeddings
- Two-layer RNN architecture
- Test Accuracy: 48.78%

### Long Short-Term Memory (LSTM)

- Word2Vec embeddings
- Two-layer LSTM architecture
- Test Accuracy: 66.20%

### Gated Recurrent Unit (GRU)

- Word2Vec embeddings
- Two-layer GRU architecture
- Test Accuracy: 62.21%

### BERT

- Pre-trained bert-base-uncased model
- Bidirectional contextual embeddings
- Test Accuracy: 68.44%

---

## Model Performance Comparison

| Model | Representation | Test Accuracy (%) |
|---------|---------------|------------------|
| Logistic Regression | TF-IDF (1,2) | 66.27 |
| SVM | TF-IDF (1,2) | 64.82 |
| Naive Bayes | BoW | 62.19 |
| RNN | Word2Vec | 48.78 |
| GRU | Word2Vec | 62.21 |
| LSTM | Word2Vec | 66.20 |
| **BERT** | Transformer | **68.44** |

### Best Performing Model

🏆 **BERT achieved the highest test accuracy of 68.44%.**


### Key Findings

- High precision and recall for ratings 1 and 5.
- Ratings 2 and 3 were harder to classify.
- TF-IDF with Unigram + Bigram features performed best among traditional methods.
- BERT provided the best overall performance.
- Class imbalance affected classification of middle ratings.

---

## Contributors
### Group 6

- Garima Patwal
- Mitalikumari Pradipbhai Patel
- Huda Shaikh

---

## Conclusion

This project demonstrates that while traditional machine learning approaches remain strong baselines for text classification, transformer-based models significantly improve performance. BERT achieved the highest accuracy by effectively capturing contextual and semantic information from review text, making it the most effective solution for Google Maps review rating prediction.
