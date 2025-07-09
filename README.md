# 💧 Water Pump Functionality Prediction

This project predicts the operational status of water pumps using machine learning. We preprocess the data, train models including Decision Tree and Random Forest classifiers, and tune hyperparameters to improve prediction accuracy.

---

## 📌 Project Overview

Access to clean water is a major challenge in many regions. This project builds a multiclass classification model to predict whether a water pump is:

- **Functional**
- **Non-functional**
- **Functional but needs repair**

By accurately identifying pump status, NGOs and local governments can prioritize maintenance and improve water access.

---

## 📂 Dataset

This project uses the [DrivenData Water Pump Challenge dataset](https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/), which contains:

- `data/train_features.csv`: Training data with features.
- `data/train_labels.csv`: Corresponding labels for training.
- `data/test_features.csv`: Test data for which we generate predictions.

The dataset includes features such as location, installer, construction year, water quality, and pump type. Some columns had too many unique categories or redundant values, so they were cleaned or dropped during preprocessing. A custom `wrangle()` function was used to remove high-cardinality and duplicate features to improve model performance.

---


## 🚀 How to Use This Repository
1.  Run the Jupyter notebook `water-pump.ipynb` to reproduce the analysis, training, and generate predictions.
2.  The predictions file `output/predictions.csv` will be created after running the model.


---

## 🔧 Key Features

- ✅ Custom `wrangle()` function for data cleaning and preprocessing  
- 📊 Automated Exploratory Data Analysis using `ydata_profiling`  
- 🔄 Train-validation splitting with baseline accuracy evaluation  
- 🌳 Decision Tree classifier pipeline with hyperparameter tuning on tree depth  
- 🌲 Random Forest classifier with hyperparameter tuning and cross-validation  
- 📈 Feature importance visualization based on Gini importance scores  
- 🔎 Randomized search for optimized hyperparameters using `RandomizedSearchCV`

---

## 📦 Requirements

This project uses the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `category_encoders`
- `ydata_profiling`


### 🔍 Interpretation 

Key insights from the data:
- Pumps installed by larger funders and in certain regions tend to be more functional.
- Older pumps have a higher chance of being non-functional.
- Some features, like `quantity` and `extraction_type`, showed strong predictive power.

### 🤖 Model & Prediction Overview

A Decision Tree Classifier was used within a pipeline that handles encoding and missing values. Multiple tree depths were tested to balance overfitting and underfitting. Feature importance scores were extracted to understand which variables had the most impact on predictions.

- **Baseline accuracy** (guessing the most frequent class): ~54%
- **Final model validation accuracy**: ~73%
- **Top features** included: `quantity`, `water_quality`, `region`, and `extraction_type`

### 📈 What the Predictions Mean

The final model can classify whether a pump is likely to:
- Be in good working condition
- Be broken
- Require minor repairs

This kind of model can support real-time decision-making by field teams or policy planners. It also demonstrates how structured data, when cleaned and modeled effectively, can provide meaningful insights for public infrastructure challenges.
