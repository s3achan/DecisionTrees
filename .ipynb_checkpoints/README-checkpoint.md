# 🌳 Decision Trees — From Theory to Practice 

This repository demonstrates **Decision Tree classification** concepts from the ground up, combining **manual impurity calculations** with **library-based implementations** using a realistic **Formula 1 race outcome dataset**.

The project is designed to show how **data noise, feature interactions, and tree depth** influence model behavior, interpretability, and overfitting.

---

## 📌 Project Objectives

- Understand **Gini impurity** and **Information Gain**
- Implement **manual decision tree logic**
- Compare **noisy vs less-noisy datasets**
- Train and visualize **DecisionTreeClassifier** using scikit-learn
- Interpret decision tree splits in a **domain-specific context (F1 racing)**

---

## 🏎️ Dataset Overview

The dataset models whether a driver finishes on the **podium** based on race-day conditions.

### Features
- `Starting_Position` — Front / Mid / Back
- `Weather` — Dry / Wet
- `Pit_Strategy` — OneStop / TwoStop
- `Safety_Car` — Yes / No

### Target
- `PodiumFinish` — Yes / No

Two dataset variants are used:
- **Highly noisy dataset** → demonstrates overfitting and deep trees
- **Less noisy dataset** → highlights clear rules such as  
  *Starting position combined with safety car presence in wet conditions*

---

## 🧠 Key Concepts Covered

- Gini impurity calculation (manual)
- Information gain (Gini reduction)
- Root node selection
- Feature interaction effects
- Tree depth vs interpretability
- Impact of noise on decision trees
- Overfitting and the need for pruning

---

## 🌳 Model Implementation

- Categorical features are **one-hot encoded**
- Decision tree trained using:
  - `criterion='gini'`
  - Controlled depth for interpretability
- Trees are visualized using `plot_tree`
- Node-level interpretations provided for each split

---

## 📊 Example Insight

> Starting position is the dominant predictor of podium finishes.  
> However, under wet conditions with safety car deployment, mid-grid drivers gain a strategic advantage, demonstrating how feature interactions shape decision boundaries.

---

## 🛠️ Tech Stack

- Python
- pandas
- numpy
- scikit-learn
- matplotlib
- Jupyter Notebook

---

## 📁 Repository Structure

