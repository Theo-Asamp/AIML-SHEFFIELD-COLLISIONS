# Sheffield Road Collision Analysis & Machine Learning

## 📌 Project Overview

This project analyses road collision data for Sheffield using machine learning techniques. The aim is to explore patterns in road accidents and develop predictive models to understand accident severity, casualty counts, and underlying risk factors.

The workflow follows an end-to-end machine learning pipeline including data preprocessing, exploratory data analysis (EDA), regression, classification, clustering, and performance evaluation.

---

## 📊 Dataset

The dataset used is:

* `dft-road-casualty-statistics-collision-1979-latest-published-year.csv`

This dataset contains UK road collision data with 44 variables, including:

* Collision severity
* Number of vehicles and casualties
* Weather and lighting conditions
* Road characteristics
* Location data

Only Sheffield data was selected using:

* `local_authority_ons_district = "E08000019"`

---

## ⚙️ Installation

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 📁 Project Structure

```
project/
│
├── data/
│   ├── raw/
│   └── processed/
│       └── sheffield_collisions.csv
│
├── notebooks/
│   └── final_notebook.ipynb
│
├── results/
│   ├── plots/
│   └── outputs/
│
└── README.md
```

---

## 🚀 Usage

1. Open the notebook:

```bash
jupyter notebook
```

2. Run all cells in order to:

* Load and filter dataset
* Perform EDA
* Train models
* Generate results and visualisations

---

## 🧹 Data Preprocessing

* Filtered dataset for Sheffield collisions
* Handled missing values
* Selected relevant features for modelling
* Encoded categorical variables using one-hot encoding

---

## 📈 Exploratory Data Analysis (EDA)

Key insights:

* Most collisions are classified as **slight**
* Majority occur at **30 mph speed limits**
* Most collisions involve **1 casualty**
* Higher speed limits show increased severity risk

Visualisations include:

* Collision severity distribution
* Speed limit distribution
* Casualties per collision
* Crosstab analysis

---

## 🤖 Machine Learning Models

### 🔹 Regression

Target:

* `number_of_casualties`

Models used:

* Linear Regression
* Random Forest Regressor

Evaluation:

* Mean Absolute Error (MAE)

---

### 🔹 Classification

Target:

* `collision_severity` (1 = Fatal, 2 = Serious, 3 = Slight)

Model used:

* Random Forest Classifier

Evaluation:

* Accuracy
* Confusion Matrix

Class imbalance was addressed using:

* `class_weight="balanced"`

---

### 🔹 Clustering

Algorithm:

* K-Means Clustering

Features:

* Number of vehicles
* Number of casualties
* Speed limit

Purpose:

* Identify patterns and group similar collision types

---

## 📊 Performance Evaluation

Metrics used:

* Accuracy (classification)
* Confusion Matrix
* Mean Absolute Error (regression)

Key findings:

* Models perform well on common cases
* Performance drops for rare events (e.g., fatal collisions)
* Class imbalance impacts classification results

---

## 📉 Key Findings

* Slight collisions dominate the dataset
* Urban areas (30 mph) have the highest collision frequency
* High-speed roads have fewer collisions but higher severity risk
* Models tend to predict the most frequent outcomes
* Rare high-casualty events are difficult to predict accurately

---

## ⚠️ Limitations

* Class imbalance affects classification performance
* Limited feature engineering
* Some missing values in location-based variables
* Models struggle with rare events

---

## 🧠 Responsible AI

This project considers:

* Bias due to class imbalance
* Limitations in predictive accuracy
* Transparency in model evaluation
* Ethical use of collision data

Models were evaluated carefully to avoid misleading conclusions.

---

## 📌 Future Improvements

* Add more advanced models (e.g., Gradient Boosting)
* Perform hyperparameter tuning
* Improve feature engineering
* Apply cross-validation
* Use geospatial analysis for hotspot detection

---

## 🤖 AI Prompts Log

AI tools were used to assist with:
- Structuring the notebook
- Debugging code issues
- Improving explanations and clarity
- Generating documentation

All outputs were reviewed, verified, and adapted by the author.

---

## 🤖 AI Transparency Statement (AITS Level 2)

AI tools were used to support structuring, explanation, and refinement of this work. These tools assisted in improving clarity, generating ideas, and debugging code.

All machine learning implementation, analysis, and final decisions were developed, verified, and critically evaluated by me.

---

## 📚 References

* UK Department for Transport Road Safety Data
* Scikit-learn Documentation
* Pandas Documentation
* Seaborn & Matplotlib Documentation

---

## 📎 Notes

* All code is written in Python
* Notebook is fully reproducible
* Ensure correct file paths before running

---
