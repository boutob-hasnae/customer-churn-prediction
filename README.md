# 📡 Customer Churn Prediction

### Turning customer data into actionable insights with Machine Learning.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="Scikit-learn"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter"/>
</p>

---

## 🎯 The Mission

**Why do customers leave, and can Machine Learning help us anticipate their decisions?**
Customer churn is a major challenge for telecommunications companies. Losing customers affects revenue, growth, and long-term customer relationships.

In this project, I explore customer behavior and build classification models to identify customers who are likely to leave a telecommunications service.

The goal is not just to predict churn, but to understand the patterns behind it.

## 📊 The Dataset


**Telco Customer Churn** — [Explore the dataset on Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

| Property | Description |
|---|---|
| Domain | Telecommunications |
| Task | Binary classification |
| Observations | 7,043 customers |
| Features | 20 input features, plus the customer identifier |
| Target | `Churn` — Yes or No |

The dataset contains information about customer demographics, subscriptions, contract types, services, payment methods, and charges.

## 🔬 The Experiment Pipeline

This project follows a structured Machine Learning workflow:

**01 — Data Exploration**  
Investigate customer characteristics, distributions, and potential churn patterns.

**02 — Data Cleaning**  
Handle missing values and convert data into appropriate types.

**03 — Exploratory Data Analysis**  
Visualize churn patterns across contracts, tenure, monthly charges, and payment methods.

**04 — Feature Engineering & Preprocessing**  
Separate input features from the target, scale numerical variables, and encode categorical variables.

**05 — Model Training**  
Train and compare two classification algorithms:

- Logistic Regression
- Random Forest Classifier

**06 — Model Evaluation**  
Evaluate model performance using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix and ROC curve

**07 — Feature Importance**  
Investigate which features contribute most to the model's predictions.

## 🧠 Models Under Investigation

| Model | Why use it? |
|---|---|
| Logistic Regression | A strong baseline with interpretable coefficients |
| Random Forest | Captures nonlinear patterns and feature interactions |

Both models are evaluated on a held-out test set. Preprocessing is fitted on training data through Scikit-learn pipelines to reduce data leakage.

## 📈 Results

The experiments compare both models using the same test set.

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 0.7381 | 0.7828 |
| Precision | 0.5043 | 0.6181 |
| Recall | 0.7834 | 	0.4759 |
| F1-score | 0.6136 | 0.5378 |
| ROC-AUC | 0.8413 | 0.8220 |


The final model should be selected based on the evaluation metrics and the project's objective, rather than accuracy alone. In a churn prediction task, recall can be particularly important because missing a customer who is about to leave may be costly.

### Key Findings

Logistic Regression achieved the highest Recall (0.7834), F1-score (0.6136), and ROC-AUC (0.8413), making it a promising choice when identifying customers at risk of churn is the main priority.

Random Forest achieved a higher Accuracy (0.7828) and Precision (0.6181), but its Recall was lower (0.4759).

These results illustrate why model selection should depend on the business objective rather than accuracy alone. Further experiments with decision thresholds and class imbalance handling could improve churn detection.

## 🛠️ Tech Stack

- **Language:** Python
- **Data manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Dataset access:** KaggleHub
- **Environment:** Jupyter Notebook / PyCharm

## 📁 Project Structure

```text

Customer-Churn/
├── notebooks/
│   └── customer_churn_prediction.ipynb
├── data/
├── requirements.txt
├── .gitignore
└── README.md

```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/boutob-hasnae/customer-churn-prediction.git
cd customer-churn-prediction
```


### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `notebooks/customer_churn_prediction.ipynb` and run the cells in order.

The notebook downloads the dataset through KaggleHub. An internet connection is required.

## 💡 Key Learning Objectives

Through this project, I practiced:

- Exploratory data analysis and data visualization.
- Numerical and categorical data preprocessing.
- Building reproducible Scikit-learn pipelines.
- Training and comparing classification models.
- Evaluating classification performance beyond accuracy.
- Interpreting feature importance and model predictions.

## ⚠️ Limitations

This is an educational Machine Learning project based on historical customer data. Model predictions indicate estimated churn risk, not certainty. Performance may vary with new data, and feature importance does not establish causation.

## 👩‍💻 About This Project

Built as part of my journey in **Artificial Intelligence and Machine Learning**, with a focus on experimentation, model evaluation, and understanding how data-driven systems work.

**Learning by experimenting. Improving by measuring. Building with purpose.**

---

<p align="center">
  <i>Customer behavior is data. Churn prediction is the experiment.</i>
</p>

