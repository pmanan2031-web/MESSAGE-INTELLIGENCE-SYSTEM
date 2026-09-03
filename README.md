# 📩 Spam Message Classification

<p align="center">
  <img src="assets/01_hero_spam_classification.png" alt="Spam Message Classification" width="100%">
</p>

<h3 align="center">
  🚀 End-to-End Machine Learning System for Spam Detection
</h3>

<p align="center">
  <b>KNN • SVM • Naive Bayes • Probability • Preprocessing • Model Evaluation</b>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Python-3.13-blue?style=for-the-badge&logo=python"></a>
  <a href="#"><img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas"></a>
  <a href="#"><img src="https://img.shields.io/badge/NumPy-Numerical%20Computing-013243?style=for-the-badge&logo=numpy"></a>
  <a href="#"><img src="https://img.shields.io/badge/Scikit--learn-ML-orange?style=for-the-badge&logo=scikit-learn"></a>
  <a href="#"><img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter"></a>
</p>

<p align="center">
  <i>From probability fundamentals to practical spam classification — one complete ML workflow.</i>
</p>

---

## 🎬 Project Demo

<p align="center">
  <img src="assets/06_spam_classification_workflow.gif"
       alt="Spam Classification Workflow"
       width="92%">
</p>

<p align="center">
  <b>📌 Complete workflow:</b>
  Data → Preprocessing → KNN → SVM → Naive Bayes → Evaluation → Business Decision
</p>

---

## 📌 Table of Contents

* [🎯 Project Overview](#-project-overview)
* [💡 Problem Statement](#-problem-statement)
* [🎯 Project Objectives](#-project-objectives)
* [📊 Dataset Overview](#-dataset-overview)
* [🧠 Probability Foundation](#-probability-foundation)
* [🔄 Machine Learning Pipeline](#-machine-learning-pipeline)
* [🤖 Machine Learning Models](#-machine-learning-models)
* [📈 Model Comparison](#-model-comparison)
* [📊 Evaluation Metrics](#-evaluation-metrics)
* [🔲 Confusion Matrix](#-confusion-matrix)
* [⚠️ Performance Validation](#️-performance-validation)
* [💼 Business Interpretation](#-business-interpretation)
* [🛠️ Technology Stack](#️-technology-stack)
* [📁 Project Structure](#-project-structure)
* [▶️ How to Run](#️-how-to-run)
* [📚 Key Learning Outcomes](#-key-learning-outcomes)
* [🚀 Future Improvements](#-future-improvements)
* [⭐ Final Takeaway](#-final-takeaway)

---

# 🎯 Project Overview

**Spam Message Classification** is an end-to-end machine learning project designed to classify messages into **Spam** and **Non-Spam** categories.

The project combines:

* Probability fundamentals
* Conditional Probability
* Bayes' Theorem
* Naive Bayes
* K-Nearest Neighbors
* Support Vector Machine
* Missing-value imputation
* Feature scaling
* Train/Test splitting
* Cross-validation
* Model comparison
* Confusion Matrix
* Precision, Recall and F1 Score
* Business-oriented model interpretation

The goal is not only to build a classifier, but also to understand **why different classification algorithms work and how their performance should be evaluated.**

---

# 💡 Problem Statement

Unwanted spam messages can affect:

* 📱 Users
* 📧 Communication systems
* 🏢 Businesses
* 🔐 Security workflows
* 📊 Customer engagement

A machine learning model can learn patterns from historical message-related features and predict whether a new message should be classified as:

| Label  | Meaning  |
| ------ | -------- |
| 🟢 `0` | Non-Spam |
| 🔴 `1` | Spam     |

The main objective is to build a classification workflow that can identify spam while minimizing incorrect classifications.

---

# 🎯 Project Objectives

### Primary Objectives

✅ Understand probability concepts used in classification
✅ Implement Conditional Probability
✅ Understand Bayes' Theorem
✅ Apply Naive Bayes classification
✅ Implement KNN classification
✅ Compare Euclidean and Manhattan distance
✅ Experiment with different K values
✅ Implement SVM with multiple kernels
✅ Handle missing values
✅ Scale numerical features
✅ Compare multiple ML models
✅ Evaluate models using classification metrics
✅ Analyze the Confusion Matrix
✅ Translate model performance into a business recommendation

---

# 📊 Dataset Overview

The supplied notebook works with a dataset containing:

| Dataset Property     |            Value |
| -------------------- | ---------------: |
| 📌 Total Records     |        **5,200** |
| 📌 Total Columns     |           **16** |
| 🎯 Target Variable   | **`spam_label`** |
| 🔢 Input Features    |           **12** |
| 🏋️ Training Records |        **4,160** |
| 🧪 Testing Records   |        **1,040** |
| 📐 Train/Test Split  |        **80/20** |
| 🎲 Random State      |           **42** |
| ⚖️ Stratification    |      **Enabled** |

### Target Variable

```text
spam_label
```

The model learns from the selected input features and predicts the target class.

---

# 🧠 Probability Foundation

<p align="center">
  <img src="assets/04_probability_bayes.png"
       alt="Probability and Bayes Theorem"
       width="95%">
</p>

## 1️⃣ Conditional Probability

Conditional probability measures the probability of an event when another event is already known.

### Formula

```text
P(A | B) = P(A ∩ B) / P(B)
```

### Spam Detection Example

Suppose:

* `A` = Message is Spam
* `B` = Message contains a URL

Then:

```text
P(Spam | URL)
```

represents the probability that a message is spam when we know that it contains a URL.

---

## 2️⃣ Bayes' Theorem

Bayes' Theorem updates the probability of an event using observed evidence.

### Formula

```text
P(A | B) = [P(B | A) × P(A)] / P(B)
```

In spam classification:

```text
P(Spam | Evidence)
```

can be estimated using the probability of observing the evidence in spam messages.

---

## 3️⃣ Naive Bayes

Naive Bayes applies Bayes' Theorem while making a simplifying assumption:

> Input features are conditionally independent given the class.

Conceptually:

```text
Features
   ↓
Probability Estimation
   ↓
Bayes' Theorem
   ↓
Class Probability
   ↓
Spam / Non-Spam
```

---

# 🔄 Machine Learning Pipeline

<p align="center">
  <img src="assets/02_ml_pipeline.png"
       alt="Machine Learning Pipeline"
       width="100%">
</p>

### Complete Workflow

```text
📂 Dataset
     │
     ▼
🔍 Data Understanding
     │
     ▼
🧹 Missing Value Handling
     │
     ▼
⚙️ KNN Imputation
     │
     ▼
📏 StandardScaler
     │
     ▼
✂️ Train/Test Split
     │
     ▼
🤖 Model Training
     │
     ├── KNN
     ├── SVM
     └── Naive Bayes
     │
     ▼
📊 Model Evaluation
     │
     ├── Accuracy
     ├── Precision
     ├── Recall
     └── F1 Score
     │
     ▼
🔲 Confusion Matrix
     │
     ▼
🏆 Model Comparison
     │
     ▼
💼 Business Recommendation
```

---

# 🧹 Data Preprocessing

## Missing Value Handling

The project uses:

```python
KNNImputer(n_neighbors=5)
```

Missing values are estimated using information from nearby observations.

---

## 📏 Feature Scaling

The project uses:

```python
StandardScaler()
```

Scaling is especially important for distance- and margin-based algorithms such as:

* KNN
* SVM

Standardization transforms features approximately to:

```text
Mean = 0
Standard Deviation = 1
```

---

# 🤖 Machine Learning Models

<p align="center">
  <img src="assets/03_theory_to_models.png"
       alt="KNN SVM Naive Bayes"
       width="100%">
</p>

---

## 🔵 1. K-Nearest Neighbors — KNN

KNN is a distance-based classification algorithm.

For a new observation:

```text
New Data Point
      ↓
Calculate Distance
      ↓
Find Nearest Neighbours
      ↓
Majority Voting
      ↓
Predicted Class
```

### K Values Tested

```text
K = 3
K = 5
K = 7
K = 9
K = 11
```

The supplied notebook selects:

```text
Best K = 3
```

based on the reported F1 score.

### Distance Metrics

The project compares:

* Euclidean Distance
* Manhattan Distance

---

## 🟢 2. Support Vector Machine — SVM

SVM is a margin-based classification algorithm.

Its objective is to find a decision boundary that separates classes effectively.

### Kernels Tested

| Kernel     | Purpose                      |
| ---------- | ---------------------------- |
| Linear     | Linear decision boundary     |
| RBF        | Non-linear decision boundary |
| Polynomial | Polynomial decision boundary |

Conceptually:

```text
Data Points
     ↓
Find Decision Boundary
     ↓
Maximize Margin
     ↓
Support Vectors
     ↓
Classification
```

---

## 🟣 3. Naive Bayes

Naive Bayes is a probability-based classifier.

The project uses:

```python
GaussianNB()
```

It estimates the probability of each class and selects the class with the highest posterior probability.

---

# 📈 Model Comparison

<p align="center">
  <img src="assets/05_model_evaluation.png"
       alt="Model Evaluation Results"
       width="95%">
</p>

### Reported Results

| Model               | Accuracy | Precision |   Recall | F1 Score |
| ------------------- | -------: | --------: | -------: | -------: |
| 🔵 KNN              | **1.00** |  **1.00** | **1.00** | **1.00** |
| 🟢 SVM — Linear     | **1.00** |  **1.00** | **1.00** | **1.00** |
| 🟢 SVM — RBF        | **1.00** |  **1.00** | **1.00** | **1.00** |
| 🟢 SVM — Polynomial | **1.00** |  **1.00** | **1.00** | **1.00** |
| 🟣 Naive Bayes      | **1.00** |  **1.00** | **1.00** | **1.00** |

### 🏆 Best Reported Model

```text
KNN
```

The notebook selects KNN as the best model based on the reported model-selection process.

---

# 🔲 Confusion Matrix

The supplied notebook reports:

|                     | Predicted Non-Spam | Predicted Spam |
| ------------------- | -----------------: | -------------: |
| **Actual Non-Spam** |            **845** |          **0** |
| **Actual Spam**     |              **0** |        **195** |

### Results

```text
TN = 845
FP = 0
FN = 0
TP = 195
```

This corresponds to:

```text
Total Test Samples = 1,040
```

and the reported classification metrics are all:

```text
Accuracy  = 1.00
Precision = 1.00
Recall    = 1.00
F1 Score  = 1.00
```

---

# 📊 Evaluation Metrics

## 🎯 Accuracy

Measures the overall percentage of correct predictions.

```text
Accuracy =
(TP + TN) / (TP + TN + FP + FN)
```

---

## 🎯 Precision

Measures how many predicted spam messages were actually spam.

```text
Precision =
TP / (TP + FP)
```

### Business Meaning

High precision helps reduce legitimate messages being incorrectly classified as spam.

---

## 🎯 Recall

Measures how many actual spam messages were successfully detected.

```text
Recall =
TP / (TP + FN)
```

### Business Meaning

High recall helps reduce **missed spam messages**.

---

## 🎯 F1 Score

F1 Score balances precision and recall.

```text
F1 =
2 × (Precision × Recall)
/
(Precision + Recall)
```

For spam detection, F1 is useful when both false positives and false negatives matter.

---

# ⚠️ Performance Validation

The supplied notebook reports **perfect 1.00 scores across every tested model**.

While this is an excellent experimental result, perfect performance across multiple fundamentally different classifiers is unusually strong.

Therefore, before presenting this as production-level performance, the following should be verified:

### 🔍 Recommended Checks

* Check for data leakage
* Verify target-related columns are not used as features
* Check whether duplicate records exist
* Verify train/test separation
* Inspect highly predictive features
* Validate preprocessing is performed without test-data leakage
* Use cross-validation
* Test on an independent dataset
* Evaluate performance on unseen real-world messages

### 🚨 Important

> **100% test accuracy does not automatically mean a model will achieve 100% accuracy in the real world.**

The reported results should therefore be treated as **notebook-level experimental results until independently validated**.

---

# 💼 Business Interpretation

A practical spam-filtering system should balance three important objectives:

### 🔴 High Recall

Catch as much spam as possible.

```text
Goal → Reduce False Negatives
```

### 🟢 High Precision

Avoid incorrectly blocking legitimate messages.

```text
Goal → Reduce False Positives
```

### 🔵 Strong F1 Score

Maintain a practical balance between precision and recall.

```text
Goal → Balanced Classification
```

### Recommended Business Priority

```text
          SPAM FILTER
              │
       ┌──────┴──────┐
       ▼             ▼
   High Recall   High Precision
       │             │
       └──────┬──────┘
              ▼
          Strong F1
              │
              ▼
      Reliable Detection
```

---

# 🛠️ Technology Stack

| Technology          | Purpose                          |
| ------------------- | -------------------------------- |
| 🐍 Python 3.13      | Programming                      |
| 🐼 Pandas           | Data manipulation                |
| 🔢 NumPy            | Numerical computation            |
| 🤖 Scikit-learn     | Machine learning                 |
| 📓 Jupyter Notebook | Development & experimentation    |
| 📊 Matplotlib       | Visualization                    |
| 🧠 KNN              | Distance-based classification    |
| 🟢 SVM              | Margin-based classification      |
| 🟣 Naive Bayes      | Probability-based classification |

---

# 📁 Project Structure

```text
Spam_Message_Classification_Project/
│
├── 📄 README.md
├── 📄 PART_A_THEORY.md
├── 📓 project4.ipynb
├── 📊 Message_Intelligence_Dataset_5200.csv
│
└── 📁 assets/
    │
    ├── 🖼️ 01_hero_spam_classification.png
    ├── 🖼️ 02_ml_pipeline.png
    ├── 🖼️ 03_theory_to_models.png
    ├── 🖼️ 04_probability_bayes.png
    ├── 🖼️ 05_model_evaluation.png
    └── 🎬 06_spam_classification_workflow.gif
```

---

# ▶️ How to Run

## 1️⃣ Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

## 2️⃣ Open the Project Folder

```bash
cd Spam_Message_Classification_Project
```

## 3️⃣ Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

## 4️⃣ Launch Jupyter Notebook

```bash
jupyter notebook
```

## 5️⃣ Open the Notebook

Open:

```text
project4.ipynb
```

Make sure the dataset is located in the same project directory:

```text
Message_Intelligence_Dataset_5200.csv
```

Then run the notebook cells sequentially.

---

# 📚 Key Learning Outcomes

By completing this project, the following concepts are demonstrated:

### Probability

* Conditional Probability
* Bayes' Theorem
* Posterior Probability
* Evidence

### Data Preprocessing

* Missing-value handling
* KNN Imputation
* Feature Scaling
* Standardization

### Classification

* K-Nearest Neighbors
* Euclidean Distance
* Manhattan Distance
* Support Vector Machine
* Linear Kernel
* RBF Kernel
* Polynomial Kernel
* Naive Bayes

### Evaluation

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* Cross-validation
* Model comparison

### Business Understanding

* False Positive
* False Negative
* Spam detection trade-offs
* Precision vs Recall
* Model selection

---

# 🚀 Future Improvements

To move this project closer to a production-ready spam detection system, the following improvements can be added:

### 🔮 1. Real Text-Based NLP

Add:

* TF-IDF
* Bag of Words
* N-grams
* Text preprocessing
* Word/character features

### 🔮 2. Advanced Models

Experiment with:

* Logistic Regression
* Random Forest
* Gradient Boosting
* XGBoost
* Linear SVM

### 🔮 3. Hyperparameter Tuning

Use:

```text
GridSearchCV
RandomizedSearchCV
```

to optimize model parameters.

### 🔮 4. Robust Validation

Add:

```text
Stratified K-Fold Cross-Validation
```

and evaluate the model on an independent dataset.

### 🔮 5. Deployment

Create a simple prediction interface using:

```text
Streamlit
```

Example:

```text
Enter Message
      ↓
Preprocessing
      ↓
Trained Model
      ↓
Prediction
      ↓
🚨 SPAM / ✅ NOT SPAM
```

---

# 🏆 Project Highlights

<p align="center">

| ⭐ Feature                | Implementation |
| ------------------------ | -------------- |
| Probability Theory       | ✅              |
| Bayes' Theorem           | ✅              |
| Naive Bayes              | ✅              |
| KNN                      | ✅              |
| SVM                      | ✅              |
| Multiple Kernels         | ✅              |
| Missing Value Imputation | ✅              |
| Feature Scaling          | ✅              |
| Cross-Validation         | ✅              |
| Confusion Matrix         | ✅              |
| Model Comparison         | ✅              |
| Business Interpretation  | ✅              |

</p>

---

# ⭐ Final Takeaway

This project demonstrates a complete journey from **mathematical probability concepts to practical machine learning classification**.

```text
Conditional Probability
        ↓
   Bayes' Theorem
        ↓
   Naive Bayes
        ↓
Data Preprocessing
        ↓
 ┌──────┼────────┐
 ▼      ▼        ▼
KNN    SVM    Naive Bayes
 └──────┼────────┘
        ↓
 Model Evaluation
        ↓
Precision • Recall • F1
        ↓
Confusion Matrix
        ↓
Business Interpretation
```

### 🏅 Reported Outcome

The supplied notebook reports:

```text
🏆 Best Model → KNN

Accuracy  → 1.00
Precision → 1.00
Recall    → 1.00
F1 Score  → 1.00
```

These results are **experimental notebook results** and should be independently validated before being interpreted as production-level performance.

---

## 👨‍💻 Project Summary

> **Spam Message Classification** demonstrates how probability, preprocessing and multiple machine learning algorithms can be combined to build an end-to-end classification workflow.

The project focuses not only on prediction accuracy, but also on **understanding the mathematical foundation, model behavior, evaluation metrics and real-world business trade-offs involved in spam detection.**

---

<p align="center">
  <b>🚀 Built with Python • Pandas • NumPy • Scikit-learn • Jupyter Notebook</b>
</p>

<p align="center">
  ⭐ If you found this project useful, consider giving the repository a star!
</p>
