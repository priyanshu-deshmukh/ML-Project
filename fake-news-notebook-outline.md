# Fake News Classification — Step-by-Step Notebook Template

---

## 1. Introduction
- Briefly describe the problem of fake news detection.
- State the goal: To classify news articles as real or fake using two machine learning models.


## 2. Dataset Loading
- Import Python libraries (`numpy`, `pandas`, `sklearn`, etc.).
- Load the first dataset (WELFake).
- Display a few rows from the dataset.
- Print basic statistics (number of rows, columns, missing values).


## 3. Data Preprocessing
- Merge title + text where necessary (or use suitable text columns).
- Lowercase text, remove punctuation, extra spaces.
- Remove stop words.
- Apply stemming or lemmatization.
- Handle missing values (drop or fill).
- Encode labels (0/1 or fake/real as needed).
- Display the processed dataset


## 4. Exploratory Data Analysis (EDA)
- Plot class distribution (fake vs real).
- (Optional) Show most common words (word cloud).


## 5. Train-Test Split
- Stratified train-test split for each dataset (e.g., 75/25 split).


## 6. Feature Extraction
- Use `CountVectorizer` or `TfidfVectorizer` from sklearn for text to vector transformation.


## 7. Model Training — Model 1
- Model 1: Multinomial Naive Bayes.
- Train the dataset.
- Predict on test set.


## 8. Model Training — Model 2
- Model 2: Logistic Regression.
- Train on the dataset.
- Predict on test sets.


## 9. Model Evaluation
- Calculate accuracy, precision, recall, F1-score for both models.
- Plot confusion matrix.
- Display results in a table for comparison.


## 10. Model Comparison
- Analyze and compare model performance (accuracy, speed, best/worst cases).
- Discuss differences observed across dataset and algorithms.


## 11. Conclusion
- Summarize key findings: Which model worked best and why.
- Suggest possible improvements/future work (more features, deep learning, ensemble methods, etc.).


## 12. Appendix
- Include all code cells for reference.
- List dataset sources and relevant literature/references.


---

> **All code cells in the notebook should have detailed markdown explanations, documenting the purpose, procedure, and expected output of each step.**

> **Tip:** For each heading, start with a markdown cell describing what will happen, then a code cell with comments explaining each code segment.