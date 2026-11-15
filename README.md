### Fake News Detection — Capstone Project
This project builds a complete Fake News Detection system using both
traditional Machine Learning models and a Neural Network (LSTM).
The dataset consists of two files:

true.csv → real news

fake.csv → fake news

I combined, cleaned, and processed both files to build the final dataset.

## 📁 Project Structure
Capstone/
│
├── data/
│      ├── true.csv
│      └──  fake.csv
│
├── notebooks/
│      ├── 01_cleaning.ipynb
│      ├── 02_ml_models.ipynb
│      └── 03_neural_network.ipynb
│
├── reports/
│      └── report.pdf
│
└── README.md

1. Data Cleaning (01_cleaning.ipynb)
In this notebook, I:

Loaded true.csv and fake.csv

Added labels:

0 → real news

1 → fake news

Combined both files into one dataset

Cleaned the text by:

Lowercasing

Removing punctuation

Removing non‑alphabetic characters

Removing stopwords

Saved the final cleaned dataset as cleaned_fake_news.csv

2. Machine Learning Models (02_ml_models.ipynb)
✔ Train/Test Split
I used an 80/20 split with stratification.

✔ TF‑IDF Vectorization
Converted text into numerical features using TF‑IDF (max_features=5000).

✔ Models Trained:
Logistic Regression

Random Forest

KNN

✔ Evaluation Metrics:
Accuracy

Precision

Recall

F1‑Score

Confusion Matrix

Best Model
Logistic Regression achieved the highest F1‑score
and performed best on high‑dimensional TF‑IDF vectors.

3. Neural Network Model (03_neural_network.ipynb)
✔ Tokenization
Converted text into integer sequences using Keras Tokenizer.

✔ Padding
All sequences padded to a fixed length (200).

✔ LSTM Architecture:
Embedding(10000, 64)

LSTM(64)

Dense(32, relu)

Dense(1, sigmoid)

Dropout layers to reduce overfitting

✔ Training
10 epochs, batch size 64.

✔ Evaluation
Generated a classification report and accuracy score on the test set.

Final Comparison
Model	Strengths	Notes
Logistic Regression	Best F1‑score, fast	Best ML model
Random Forest	Decent performance	Not ideal for sparse TF‑IDF
KNN	Weakest	High dimensionality hurts performance
LSTM Neural Network	Learns sequence patterns	Requires more training time


Conclusion
Both approaches (ML + LSTM) successfully classify fake vs real news.
Logistic Regression performed best among ML models,
while the LSTM model captured deeper language patterns.

This project demonstrates:

Text preprocessing

Feature extraction

ML model training

Neural network modeling

Evaluation and comparison

Author
# Zeyad Talal Al‑Mashuoq (201)  
Capstone Project
