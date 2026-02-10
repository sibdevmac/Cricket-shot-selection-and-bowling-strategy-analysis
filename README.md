# 🏏 Cricket Shot Selection & Bowling Strategy Analytics

## 📌 Project Overview

With the ICC T20 leagues in full swing, data-driven decision making has become essential for optimizing bowling strategies and field placements.

This project analyzes a cricket shot selection dataset to understand **how bowling mechanics, physics, and tactics influence runs conceded and wicket probability**.

Dataset source:
👉 [https://www.kaggle.com/datasets/piyushsharma18/cricket-shot-selection](https://www.kaggle.com/datasets/piyushsharma18/cricket-shot-selection)

The dataset contains ball-by-ball attributes such as:

* Bowler Type
* Ball Length
* Ball Line
* Speed (km/h)
* Shot Type
* Runs Scored
* Wicket
* Field Placement
* Angle
* Bounce (cm)
* Field Positions

These variables allow both **statistical** and **physics-based (trajectory, bounce, speed)** analysis of cricket outcomes.

---

## 🎯 Research Objectives

### Primary Question

**How do bowling characteristics (length, line, speed, bounce) influence runs and wicket probability, and what strategies are most effective?**

### Secondary Research Questions

| ID  | Question                                                                     |
| --- | ---------------------------------------------------------------------------- |
| RQ1 | Which length + line combinations minimize runs and maximize wickets?         |
| RQ2 | Which shots produce the highest scoring efficiency and which are most risky? |
| RQ3 | Does bowling speed affect runs and wicket probability?                       |
| RQ4 | Which field placements suppress scoring or increase dismissals?              |
| RQ5 | Can wickets be predicted using ball characteristics (machine learning)?      |

---

## 📊 Key Findings

### 🔹 RQ1 — Length + Line Strategy

Best combinations (lowest runs conceded):

* Full + Off stump
* Good + Off stump
* Good + Leg stump

Worst combinations (high scoring zones):

* Good + Middle
* Short + Leg

**Insight:**
Bowling outside off stump with fuller/good lengths reduces the batter’s scoring arc and increases defensive shots or edges.

---

### 🔹 RQ2 — Shot Efficiency

Runs per ball analysis shows:

Highest scoring shots:

* Pull
* Straight drive
* Hook
* Flick

Medium:

* Cover drive
* Cut
* Defensive

Lowest scoring:

* Sweep
* Edge

**Insight:**
Short leg-side or full straight deliveries enable aggressive power shots.
Outside-off good lengths force defensive or edge outcomes.

---

### 🔹 RQ3 — Speed vs Performance

| Speed Range      | Insight                                  |
| ---------------- | ---------------------------------------- |
| 136–142 km/h     | Highest wicket rate (~5.6%)              |
| 142–149 km/h     | Most economical (lowest runs)            |
| 116–123, 129–136 | Worst trade-off (high runs, low wickets) |

**Physics interpretation:**

* Higher speed → less reaction time
* Higher kinetic energy → sharper bounce variation
* More mistimed shots → more wickets

---

### 🔹 RQ4 — Field Placement Impact

| Field Type | Effect                     |
| ---------- | -------------------------- |
| Aggressive | Lowest runs (best economy) |
| Defensive  | Highest wickets            |
| Balanced   | Worst overall performance  |

**Insight:**

* Aggressive fields create pressure and reduce scoring
* Defensive fields induce risky aerial shots
* Balanced fields provide neither control nor traps

---

### 🔹 RQ5 — Wicket Prediction (Machine Learning)

Models were built using:

* Logistic Regression
* Random Forest
* Encoded categorical variables
* Ball physics features

Key learning:

* Accuracy alone (~94%) is misleading due to class imbalance
* ROC-AUC (~0.52) indicates weak predictive power
* Wickets depend on additional contextual features (shot type, field, match state)

**Conclusion:**
Ball characteristics alone are insufficient for strong wicket prediction.
Adding tactical and contextual variables is necessary for reliable modeling.

Reference study:
Optimal model for predicting highest runs chase outcomes in T20 cricket
Prediction efficiency ~92%
[https://www.sciencedirect.com/science/article/pii/S1110016824015837](https://www.sciencedirect.com/science/article/pii/S1110016824015837)

---

## ⚙️ Methods Used

* Exploratory Data Analysis
* Heatmaps
* Field strategy mapping
* Logistic Regression

Libraries:

* pandas
* numpy
* matplotlib
* seaborn
* scikit-learn

---

## 🧠 Tactical Recommendations

### For Economy

* Full/Good outside off
* 142+ km/h
* Aggressive field

### For Wickets

* 136–142 km/h
* Good length channel
* Defensive/deep catching field

### Avoid

* Middle-line good length
* Medium pace comfort zones
* Balanced field setups


## 📌 Conclusion

This project demonstrates how **data science + physics + cricket tactics** can optimize bowling decisions.

Small adjustments in:

* speed
* length
* line
* field placement

can significantly change match outcomes.

Analytics can therefore serve as a practical decision-support tool for modern T20 strategy.
