# 🛒 Binary Classification for Product Matching  



---

## 📌 Project Overview  
This dissertation investigates the **product matching problem** in e-commerce, where the goal is to determine whether two product listings from different platforms refer to the same real-world item.  

The problem is framed as a **binary classification task**:  
- **Match (1):** Same product  
- **Non-Match (0):** Different products  

The study uses **JSON-formatted datasets** with product titles, descriptions, specifications, prices, and metadata. Key challenges included **handling nested structures, missing values, class imbalance, and heterogeneous textual data**.  

---

## 🔑 Key Contributions  
- **Data Preprocessing**: Flattened hierarchical JSON structures, imputed missing values, removed duplicates, and standardized attributes.  
- **Feature Engineering**:  
  - Combined textual attributes into a single `combined_text` column.  
  - Applied **TF-IDF vectorization** to capture semantic similarities.  
- **Class Imbalance Handling**: Used **SMOTE (Synthetic Minority Over-sampling Technique)** to balance minority and majority classes.  
- **Model Development**: Implemented and compared **Logistic Regression, Naïve Bayes, Decision Tree, and Random Forest**.  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-score, Confusion Matrices, and Cross-validation.  
- **Visualization**: Used word clouds, heatmaps, bar charts, and performance plots to interpret results.  

---

## 🧪 Models & Results  
| Model | Accuracy | Precision (Match) | Recall (Match) | F1-score (Match) | Notes |  
|-------|----------|-------------------|----------------|------------------|-------|  
| **Logistic Regression** | 89% | 47% | 78% | 59% | Good baseline, improved after SMOTE but limited by linear assumptions. |  
| **Decision Tree** | 88% | 57% | 63% | 60% | Interpretable, handles non-linear data but prone to overfitting. |  
| **Naïve Bayes** | 66% | 23% | 59% | 33% | Lightweight, struggled with correlated text features. |  
| **Random Forest** | 92% | 76% | 59% | 66% | Best performer: robust, handles non-linearity, reduces overfitting. |  

---

## ⚙️ Tech Stack  
- **Python** (Pandas, NumPy, scikit-learn, imbalanced-learn)  
- **Google Colab** (cloud-based training environment)  
- **Matplotlib & Seaborn** (visualizations)  

---

## 📊 Workflow Summary  
1. **Data Collection & Preprocessing**  
   - Flattened nested JSON fields  
   - Imputed missing numerical & categorical values  
   - Removed duplicates & irrelevant attributes  

2. **Exploratory Data Analysis (EDA)**  
   - Analyzed text length distributions, missing values, and class imbalance  
   - Generated histograms, word clouds, and heatmaps  

3. **Feature Engineering**  
   - Combined textual fields → `combined_text`  
   - Applied **TF-IDF vectorization (max_features=5000)**  

4. **Model Training & Evaluation**  
   - Logistic Regression, Decision Tree, Naïve Bayes, Random Forest  
   - Used **SMOTE** to balance data  
   - Evaluated via accuracy, precision, recall, F1-score, and cross-validation  

5. **Best Model**: **Random Forest** achieved **92% accuracy** with balanced precision and recall.  

---

## 🚀 Future Work  
- Explore **deep learning approaches** (e.g., BERT embeddings for semantic matching)  
- Implement **hybrid models** (rule-based + ML)  
- Apply **explainable AI (XAI)** for feature importance and interpretability  
- Test scalability on **large-scale e-commerce datasets**  

---

## 📚 References  
- Breiman, L. (2001). *Random Forests*. Machine Learning.  
- Chawla, N. V., et al. (2002). *SMOTE: Synthetic Minority Over-sampling Technique*.  
- Christen, P. (2012). *Data Matching: Concepts and Techniques for Record Linkage, Entity Resolution, and Duplicate Detection*.  
- Mudgal, S., et al. (2018). *Deep Learning for Entity Matching*.  
- University of Greenwich MSc Dissertation Guidelines (2024).  

---Article Publication 
https://zenodo.org/records/21837871

