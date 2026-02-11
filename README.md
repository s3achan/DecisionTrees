# 🏎️ F1 Podium Prediction using Decision Trees  
### Gini Impurity & Entropy (Information Gain)

This project demonstrates how **Decision Tree classifiers** work from **start to finish**, both **manually (from first principles)** and using **scikit-learn**. The goal is to predict whether a Formula 1 driver finishes on the podium based on race conditions.

The notebook covers:
- Entropy and Gini impurity theory  
- Manual Information Gain calculations  
- Root node and split selection  
- Decision tree visualization  
- Prediction extraction  
- Gini vs Entropy comparison  
- Performance optimization of split calculations  

---

## 📊 Dataset Overview

The dataset is a **synthetic Formula 1 race dataset**, created for interpretability and learning purposes.

### Features
- **Weather**: Dry, Wet  
- **Starting_Position**: Front, Mid, Back  
- **Pit_Strategy**: OneStop, TwoStop  
- **Safety_Car**: Yes, No  

### Target Variable
- **PodiumFinish**: Yes, No  

---

## 🌳 Decision Tree Methodology

Decision Trees split data recursively to reduce impurity and improve class separation.

This project implements **two impurity measures**:

---

### 1️⃣ Entropy & Information Gain (ID3-style)

- Measures **uncertainty** in the target variable  
- Selects splits that **maximize Information Gain**  
- More sensitive to class distribution changes  

### 2️⃣ Gini Impurity (CART-style)

- Measures **probability of misclassification**  
- Faster to compute than entropy  
- Default criterion used by scikit-learn  


## 🔍 Gini vs Entropy Comparison

Both **Gini-based** and **Entropy-based** decision trees are trained and evaluated.

### Observations
- Both models produce **identical predictions** on this dataset
- Early splits (Starting Position, Weather) are consistent
- Differences mainly appear in **split order and depth** when the data is noisy

---

## 📈 Results Summary

- **Accuracy:** 78.6% (11 out of 14 predictions correct)
- Most errors occur for **mid-grid or back-grid starters**
- **Starting position** is the strongest predictor
- Weather, safety car, and pit strategy act as **secondary refinements**

---

## 🧠 Key Takeaways

- Gini and Entropy use the same split logic with different impurity measures
- Gini is faster and widely used in practice
- Entropy offers stronger theoretical interpretation
- Predictions are made via **majority vote at leaf nodes**
- Optimization improves clarity and scalability

---

## 📂 Repository Contents

- **F1-DecisionTrees-Entropy.ipynb** – Full end-to-end notebook
- **README.md** – Project overview and methodology
- Decision tree visualizations
- Manual entropy, gini, and information gain calculations

---

## 🚀 Future Improvements

- Add pruning and depth regularization
- Compare with Random Forest and Gradient Boosting
- Apply to real-world motorsport or Kaggle datasets
- Extend to probability calibration and threshold tuning
