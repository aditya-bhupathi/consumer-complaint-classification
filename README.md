# Machine Learning Models: Logistic Regression, SVM, and Naive Bayes

## Overview
This project demonstrates the application of three fundamental machine learning models:
- Logistic Regression
- Support Vector Machine (SVM)
- Naive Bayes (MultinomialNB / GaussianNB)

The dataset is loaded and used directly **without any NLP preprocessing**.  
The primary objective is to compare the performance of these classifiers on the dataset.

---

## Files
- **B V V S B Aditya.ipynb**: Jupyter Notebook containing the implementation of Logistic Regression, SVM, and Naive Bayes classifiers.

## Dataset
- source:https://catalog.data.gov/dataset/consumer-complaint-database
- This dataset is too large 6.4gb approx
- so i tried splitting data


## Requirements
To run the notebook, install the following Python libraries:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn
```

---

## Workflow
1. Load dataset (CSV or other format).
2. Split the dataset into training and testing sets.
3. Train the following models:
   - Logistic Regression
   - SVM (Support Vector Machine)
   - Naive Bayes
4. Evaluate each model using:
   - Accuracy
   - Confusion Matrix
   - Classification Report (Precision, Recall, F1-score)

---

## How to Run
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook "B V V S B Aditya.ipynb"
   ```
2. Run all cells step by step.

---

## Results
The notebook will output the evaluation metrics for each model, making it easy to compare their performance.

---

## Notes
- No NLP preprocessing (tokenization, stopword removal, stemming/lemmatization, vectorization) is included in this project.
- This project focuses **only** on classification using Logistic Regression, SVM, and Naive Bayes.

---

## Author
Prepared by **B V V S B ADITYA**.
