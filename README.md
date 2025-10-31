# 🧪 Chemical Waste Management Analysis using Double Optimization & Topic Modelling (Kotak Riset SC)

## 📘 Overview
This project analyzes and models **chemical waste management in industrial facilities across the United States** using advanced **machine learning** and **optimization techniques**.  
By combining **Particle Swarm Optimization (PSO)**, **Ant Colony Optimization (ACO)**, and **Gradient Boosting-based models**, this study predicts **waste production levels** while also integrating **public sentiment analysis** through **Twitter data (BERTweet + BERTopic)**.

Developed as part of **Kotak Riset SC (Fortex 5.0 National Data Science Competition Winner)**, this research aims to bridge **environmental data science** with **social insights**, helping improve waste reduction policies and public awareness.

---

## 🧩 Objectives
- Predict industrial **chemical waste production** using EPA’s **Toxic Release Inventory (TRI)** dataset.  
- Apply **feature engineering** and **model optimization** to enhance accuracy.  
- Extract **public sentiment** toward industrial waste management using **NLP-based topic modelling**.  
- Provide **data-driven recommendations** for policymakers and industries.

---

## 🧠 Methodology

### 1. Data Source
- **Dataset**: EPA’s [Toxic Release Inventory (TRI)](https://www.epa.gov/toxics-release-inventory-tri-program)  
- **Public Sentiment**: Tweets from January–December 2023, filtered with keywords such as *“chemical waste”*, *“toxic waste”*, and *“production waste”*.

### 2. Data Preprocessing
- **Missing value handling** using `KNNImputer`
- **Outlier detection** and removal  
- **Feature encoding** with `LabelEncoder`  
- **Standard scaling** for numerical normalization  

### 3. Feature Engineering
Created over **30 engineered features**, including:
- `Total Waste`, `Total Emission`, `Energy Recovery Ratio`, `Risk Factor`, and `Hazard Score`
- Derived ratio-based metrics (e.g., *Emission-to-Waste per Carcinogen, PBT, PFAS*)

### 4. Machine Learning Models
| Model | Technique | Description |
|-------|------------|--------------|
| **Random Forest** | Ensemble | Robust baseline model |
| **XGBoost / LightGBM** | Gradient Boosting | Leaf-wise optimized boosting |
| **CatBoost** | Gradient Boosting | Handles categorical data effectively |
| **VotingRegressor / Stacking** | Ensemble | Combines multiple models |
| **Optimizers (PSO, ACO, Hill Climb)** | Metaheuristics | Hyperparameter optimization |

### 5. Sentiment & Topic Modelling
- **Model**: BERTweet + BERTopic  
- **Library**: `pysentimiento`  
- **Goal**: Identify topics and public concerns regarding waste management policies and environmental pollution.

---

## ⚙️ Tools and Libraries
```python
pandas, numpy, matplotlib, seaborn
scikit-learn, xgboost, lightgbm, catboost
hyperopt, autogluon, shap
pysentimiento, bertopic, transformers
```

---

## 🚀 Workflow Summary
```text
Data Acquisition → Data Cleaning → Feature Engineering
→ Model Training (XGBoost, RF, LGBM, CatBoost)
→ Double Optimization (PSO + ACO)
→ Sentiment Analysis (BERTweet)
→ Topic Modelling (BERTopic)
→ Results & Visualization
```

---

## 📊 Results
| Model | MAE | RMSE | R² |
|--------|------|------|----|
| XGBoost | 100.5 | 420.5 | 0.998 |
| Gradient Boosting | 90.5 | 380.5 | 0.997 |
| Stacking + Ant Colony | 88.6 | 420.4 | 0.999 |

✅ **Best Model:** *BLENDED MODEL GRADIENT
 BOOSTING PSO + XGBOOST
 PSO + STACKING AC*  
✅ **MAE = 55.0**, **RMSE = 255.12**, **R² = 0.999**

**Sentiment Analysis Results:**
- Negative tweets dominate discussions on **food waste**, **water pollution**, and **industrial chemical disposal**.  
- **Public sentiment** highlights concern for **Clean Air Act chemicals** and **EPA policy enforcement**.

---

## 🧩 Key Insights
- Feature Engineering significantly improved model performance by >15%.  
- Optimization techniques (PSO & ACO) further reduced prediction errors.  
- Social sentiment analysis supports policy recommendations for targeted regions like **Iroquois**, **Kittson**, and **Gilman**.

---

## 🌍 Recommendations
- Strengthen off-site waste management infrastructure.  
- Enhance regulation for **classified chemical materials** (e.g., food-related waste).  
- Use **public sentiment monitoring** as an environmental feedback mechanism.  

---

## 📜 References
Includes key references from:
- **EPA TRI Program (1999–2024)**
- **Breiman (2001)** Random Forests  
- **Ke et al. (2017)** LightGBM  
- **Prokhorenkova et al. (2019)** CatBoost  
- **Nguyen et al. (2020)** BERTweet  
- **Grootendorst (2022)** BERTopic  

---

## 👥 Authors
**Krisna Bayu Dharma Putra**  
**Rhafael Chandra**  
**Vincent Yeozekiel**  
Part of **Kotak Riset SC**, *Fortex 5.0 Finalist Project*  

📧 [linkedin.com/in/dharma-putra1305](https://linkedin.com/in/dharma-putra1305)  
🌐 [github.com/kbdp1305](https://github.com/kbdp1305)
