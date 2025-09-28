## Machine Learning Models: Logistic Regression, SVM, and Naive Bayes

# Consumer Complaint Text Classification

## Project Overview

This project performs **text classification** on the Consumer Complaint Database to classify consumer complaints into categories:

| Label | Category                                                                     |
| ----- | ---------------------------------------------------------------------------- |
| 0     | Credit reporting, credit repair services, or other personal consumer reports |
| 1     | Debt collection                                                              |
| 2     | Consumer Loan                                                                |
| 3     | Mortgage                                                                     |

The project uses multiple classification models to compare performance and selects the best model for prediction.

## Steps in the Project

1. **Dataset**

   * Source: [https://catalog.data.gov/dataset/consumer-complaint-database](https://catalog.data.gov/dataset/consumer-complaint-database)
   * The raw dataset is very large (~6.4 GB).
   * Only complaints belonging to the four target categories were retained.
   * The cleaned and processed version is saved as `complaints_filtered_all.csv`.

2. **Explanatory Data Analysis (EDA) & Feature Engineering**

   * Analyzed text length distribution.
   * Count distribution of categories.
   * Created new features like `text_len`.

3. **Text Pre-processing**

   * Lowercased text.
   * Removed special characters.
   * Removed extra whitespace.

4. **Label Mapping**

   * Converted `Product` text category to numeric labels using mapping.

5. **Model Selection**

   * Logistic Regression
   * Linear Support Vector Machine (Linear SVC)
   * Multinomial Naive Bayes

6. **Comparison of Model Performance**

   * Accuracy, precision, recall, and F1-score.

7. **Model Evaluation**

   * Classification reports.

8. **Prediction**

   * Best-performing model used for predictions.

## Requirements

* Python >= 3.8
* Libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn nltk tqdm joblib
```

Additional NLTK Setup:

```python
import nltk
nltk.download('stopwords')
nltk.download('wordnet')
```

## File Structure

```
project_folder/
│
├── data/
│   ├── Consumer_Complaints_part1.csv
│   ├── Consumer_Complaints_part2.csv
│   ├── ...
│
├── notebooks/
│   ├── Consumer_Complaints_Classification.ipynb
│
├── preprocessed_data/
│   ├── complaints_filtered_all.csv
│
├── models/
│   ├── tfidf_vectorizer.joblib
│   ├── best_model_LinearSVC.joblib
│
├── README.md
```

## How to Run

1. Clone or download the repository.
2. Place dataset CSV files in the `data/` folder.
3. Adjust parameters (`base_dir`, `part_pattern`, etc.) in the notebook.
4. Install dependencies.
5. Run the notebook:

```bash
jupyter notebook notebooks/Consumer_Complaints_Classification.ipynb
```

## Example Predictions

```python
samples = [
    "I found errors on my credit report and it lowered my score.",
    "I get calls from a debt collector about a loan I never took.",
    "My consumer loan application was denied despite good credit.",
    "My mortgage servicer charged me an incorrect fee."
]

predictions = predict_texts(samples)
print(predictions)
```

## Author

B V V S B Aditya
