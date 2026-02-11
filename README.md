🏎️ F1 Podium Prediction using Decision Trees
(Gini Impurity & Entropy / Information Gain)

This project demonstrates how Decision Tree classifiers can be built from first principles and with scikit-learn, using both Gini impurity and Entropy (Information Gain) to predict whether a Formula 1 driver finishes on the podium.

The notebook walks step-by-step through:

Manual impurity calculations

Root-node selection

Tree visualization

Prediction comparison

Model evaluation

Performance optimization of split calculations

📊 Dataset Overview

The dataset is a synthetic F1 race dataset designed for interpretability.

Features

Weather (Dry / Wet)

Starting_Position (Front / Mid / Back)

Pit_Strategy (OneStop / TwoStop)

Safety_Car (Yes / No)

Target

PodiumFinish (Yes / No)

🌳 Decision Tree Approaches
1️⃣ Entropy & Information Gain (ID3-style)

Uses entropy to measure uncertainty

Selects splits that maximize Information Gain

More sensitive to class distribution changes

Core formula:

𝐼
𝐺
=
𝐸
𝑛
𝑡
𝑟
𝑜
𝑝
𝑦
(
𝑝
𝑎
𝑟
𝑒
𝑛
𝑡
)
−
∑
𝑖
∣
𝑆
𝑖
∣
∣
𝑆
∣
⋅
𝐸
𝑛
𝑡
𝑟
𝑜
𝑝
𝑦
(
𝑆
𝑖
)
IG=Entropy(parent)−
i
∑
	​

∣S∣
∣S
i
	​

∣
	​

⋅Entropy(S
i
	​

)
2️⃣ Gini Impurity (CART-style)

Uses Gini impurity to measure misclassification probability

Faster and commonly used in practice

Default criterion in scikit-learn

Core formula:

𝐺
𝑖
𝑛
𝑖
=
1
−
∑
𝑝
2
Gini=1−∑p


🔍 Model Comparison

Both Gini-based and Entropy-based decision trees are trained and compared using:

Tree visualizations

Feature importance

Prediction outputs

Accuracy and mismatches

In this dataset:

Both models produce identical predictions

Differences mainly appear in split ordering and depth under noisy conditions

📈 Results Summary

Dataset Accuracy: 78.6% (11 / 14 correct)

Most prediction errors occur for mid-grid or back-grid starters

Confirms that starting position is the dominant predictor

Secondary factors (weather, safety car, strategy) refine outcomes

🧠 Key Takeaways

Gini and Entropy follow the same split-selection logic but use different impurity measures

Gini is computationally cheaper and widely used

Entropy provides stronger theoretical interpretability

Decision trees predict outcomes by majority vote at leaf nodes

Optimization matters even for educational implementations

📂 Repository Contents

F1-DecisionTrees-Entropy.ipynb – Full notebook walkthrough

README.md – Project overview and methodology

Decision tree visualizations

Manual impurity and information gain calculations

🚀 Future Improvements

Add pruning and depth control

Extend to probabilistic calibration

Compare against Random Forest / XGBoost

Test on real F1 or motorsport datasets
