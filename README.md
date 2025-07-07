# 💧 Water Pump Functionality Prediction

Predicting the operational status of water pumps in Tanzania using machine learning.

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

- `train_features.csv` — pump characteristics  
- `train_labels.csv` — pump status labels  
- `test_features.csv` — pumps without status labels, used for final predictions

> 📁 To run the notebook, place all files in a folder named `data/` at the root of this repo.

---

## 🚀 How to Use This Repository

1. **Download the dataset** from DrivenData.
2. **Place CSV files** in a `data/` folder in this project directory.
3. **Open** the Jupyter Notebook `water-pump.ipynb`.
4. **Run** all cells to explore the data, build models, and generate predictions.

---

## 🔧 Key Features

- ✅ Data cleaning with a custom `wrangle()` function  
- 📊 Exploratory Data Analysis with `ydata_profiling`  
- 🔄 Train-validation split with baseline accuracy  
- 🌳 Decision Tree classifier with pipeline and depth tuning  
- 📈 Feature importance visualization using Gini scores

---

## 📦 Requirements

This project uses the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `category_encoders`
- `ydata_profiling`

Install all required packages with:

```bash
pip install -r requirements.txt
