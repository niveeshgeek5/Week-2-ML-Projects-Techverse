

This repository contains two Machine Learning projects implemented using Python.

## Projects Included

1. Linear Regression (Implemented Manually using NumPy)
2. Spam Email Detection using Support Vector Machine (SVM)

---

# Project 1: Linear Regression

## Objective

The objective of this project is to understand the working of the Linear Regression algorithm by implementing it manually without using Scikit-Learn.

The model predicts marks obtained by a student based on the number of study hours.

---

## Dataset

A simple manually created dataset is used.

| Study Hours | Marks |
|-------------|-------|
| 1           | 18    |
| 2           | 32    |
| 3           | 40    |
| 4           | 58    |
| 5           | 65    |



## Concepts Used

### NumPy

Used for performing mathematical calculations efficiently.

### Linear Regression

Linear Regression finds the best-fit straight line between independent and dependent variables.

Equation:

Y = b0 + b1X

Where

- X = Independent Variable (Study Hours)
- Y = Dependent Variable (Marks)
- b0 = Intercept
- b1 = Slope

---

### Slope Calculation

The slope determines how much the output changes for every unit increase in input.

Formula

b1 =

(nΣXY − ΣXΣY)
-------------------------
(nΣX² − (ΣX)²)

---

### Intercept Calculation

Formula

b0 =

(ΣY − b1ΣX)
------------
      n

---

### Prediction

Predicted values are calculated using

Y = b0 + b1X

---

### Mean Squared Error (MSE)

Measures prediction error.

Formula

MSE = Σ(Y − Ŷ)² / n

Lower MSE indicates better performance.

---

## Output

The program prints

- Slope
- Intercept
- Predicted Marks
- Mean Squared Error

---

# How to Run (Google Colab)

### Step 1

Open Google Colab

https://colab.research.google.com

### Step 2

Create a New Notebook.

### Step 3

Copy and paste the Linear Regression code.

### Step 4

Run the notebook.

No dataset upload is required because the dataset is created inside the code.

---

# Project 2: Spam Email Detection using SVM

## Objective

The objective of this project is to classify emails into

- Spam
- Not Spam (Ham)

using the Support Vector Machine (SVM) algorithm.

---

## Dataset

Dataset Used

spam.csv

Columns

- v1 → Label (Spam/Ham)
- v2 → Email Text

Labels are converted into

Spam = 1

Ham = 0

---

## Machine Learning Workflow

### 1. Upload Dataset

The dataset is uploaded using Google Colab.

```python
from google.colab import files
uploaded = files.upload()
```

---

### 2. Load Dataset

The dataset is loaded using Pandas.

---

### 3. Data Cleaning

Only the required columns are selected.

Columns are renamed

v1 → spam

v2 → text

Missing values are removed.

---

### 4. Feature Extraction

Email text cannot be directly used by machine learning algorithms.

TF-IDF Vectorization converts text into numerical values.

Benefits

- Removes stop words
- Gives higher weight to important words
- Supports unigram and bigram features

---

### 5. Train-Test Split

The dataset is divided into

- 80% Training
- 20% Testing

---

### 6. Support Vector Machine (SVM)

The model used is

LinearSVC()

SVM works by finding the best hyperplane that separates spam and non-spam emails.

Advantages

- High accuracy
- Effective for text classification
- Works well with TF-IDF features

---

### 7. Model Evaluation

The following metrics are calculated

- Accuracy
- Classification Report
- Confusion Matrix

---

### 8. Predict New Email

A custom email is provided.

The trained model predicts whether it is

- Spam
- Not Spam

---

## Libraries Used

- pandas
- scikit-learn
- google.colab

Modules

- train_test_split
- TfidfVectorizer
- LinearSVC
- accuracy_score
- classification_report
- confusion_matrix

---

# How to Run (Google Colab)

### Step 1

Open Google Colab

https://colab.research.google.com

---

### Step 2

Create a New Notebook.

---

### Step 3

Copy the SVM code into the notebook.

---

### Step 4

Download the dataset

spam.csv

---

### Step 5

Run the first cell.

A file upload window will appear.

Upload

spam.csv

---

### Step 6

Run all remaining cells.

The notebook will display

- Dataset Preview
- Dataset Shape
- Missing Values
- Accuracy
- Classification Report
- Confusion Matrix
- Prediction for New Email

---

# Expected Output

## Linear Regression

- Slope
- Intercept
- Predicted Marks
- Mean Squared Error

---

## Spam Detection

- Dataset Information
- Accuracy
- Classification Report
- Confusion Matrix
- Spam / Not Spam Prediction

---

# Folder Structure

Machine-Learning-Projects/

│

├── LinearRegression.ipynb

├── SpamDetectionSVM.ipynb

├── spam.csv

├── README.md

└── requirements.txt

---

# Requirements

Python 3.x

Libraries

numpy

pandas

scikit-learn

---

Install using

```bash
pip install numpy pandas scikit-learn
```

Google Colab already contains these libraries by default.

---

# Conclusion

The Linear Regression project demonstrates how regression works by manually calculating the slope, intercept, predictions, and Mean Squared Error using NumPy.

The Spam Email Detection project demonstrates a complete machine learning classification workflow using TF-IDF feature extraction and a Support Vector Machine (SVM). The trained model successfully classifies emails as spam or non-spam with high accuracy.
