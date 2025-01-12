# README – School Closure Prediction and Analysis by Classification & Unsupervised analysis Project

## Project Description
This project focuses on analyzing, classifying, and predicting the likelihood of school closures. The data were obtained from a government open-data website and include various features such as tuition fees, sector, number of classes, school status (open/closed), and more.

The primary goal is to identify schools that are at risk of closure in advance and to understand which features predict this risk. To achieve our goal we did two projects, one of which **Classification** project was carried out, in which multiple models (XGBoost, Random Forest, SVC, etc.) were compared to forecast whether a school is likely to remain open or close. The main focus was addressing the class imbalance issue (most data pertain to “open” schools) and selecting appropriate metrics (Precision, Recall, F1-score) to evaluate model performance.

At the same time, an **Unsupervised** analysis was also conducted to gain insights into the data structure and investigate various influences beyond what the supervised models revealed.

---

## Table of Contents
1. [Work Process – Brief Summary](#work-process--brief-summary)  
2. [Models and Methods](#models-and-methods)  
3. [Key Results](#key-results)  
4. [Future Directions](#future-directions)

---

## Work Process – Brief Summary

1. **Data Exploration (EDA)**  
   - Initial checks of distributions, detecting and removing outliers, correlation analysis, and more.

2. **Preprocessing**  
   - Removing irrelevant rows and columns (e.g., notes, empty columns).  
   - Handling missing values (dropping or imputing).  
   - Converting variables to numeric (Label Encoding, One-Hot Encoding).  
   - Dropping columns with high correlation (above 75%).  

3. **Model Training**  
   - Supervised models (SVC, Random Forest, XGBoost, GBM, Voting/Bagging).  
   - Unsupervised models (K-means, DBSCAN, GMM, Agglomerative Clustering).  

4. **Evaluation and Conclusions**  
   - Classification metrics (Precision, Recall, F1-score, etc.).  
   - Clustering metrics (Silhouette, DBI, Calinski-Harabasz, etc.).  
   - Selecting the best model and analyzing the results.

---

## Models and Methods

### Supervised Models (Classification)
1. **XGBoost** – Considered the strongest model in the project due to its robustness with imbalanced data and its ability to handle complex datasets.  
2. **Gradient Boosting Machine (GBM)** – Similar to XGBoost but generally less computationally efficient.  
3. **Random Forest** – An ensemble of decision trees that helps reduce overfitting and performs well with imbalanced data.  
4. **SVC** – Handles non-linear relationships but needs feature scaling.

### Unsupervised Models (Clustering)
1. **K-means** – Easy to understand and implement, works well if data clusters are “circular.”  
2. **DBSCAN** – Sensitive to density parameters (epsilon), suitable for data with varying densities, does not require cluster shapes to be circular.  
3. **GMM** – Assumes a normal (Gaussian) distribution; not necessarily suitable for skewed data.  
4. **Agglomerative Clustering** – Provides hierarchical grouping without the need to predefine the number of clusters.

---

## Key Results

- **Classification Models**:  
  - **XGBoost** delivered the best performance in distinguishing “closed” schools from “open” schools.  
  - Tuition fees and total salary/payments budget were among the most influential features for prediction.  
  - Focusing on Precision and Recall helped address class imbalance.

- **Unsupervised Models**:  
  - Most algorithms pointed to tuition fees as the main factor that splits the data into clusters.  
  - **K-means** performed best, likely because the data’s structure aligns more with its underlying assumptions.  
  - There is a concern that the data are “one-dimensional,” primarily driven by a single feature (tuition fees). Removing this feature significantly harmed clustering quality.

---

## Future Directions

1. **Handling Class Imbalance**: Using synthetic data (e.g., SMOTE) or over-/undersampling techniques.  
2. **Data Enrichment (Feature Engineering)**: Attempting to add or compute new features (e.g., averages, ratios between features).  
3. **Real-Time / Time-Series Data**: Collecting historical and future data for more accurate forecasts and earlier risk detection.  
4. **Improvements in Clustering Algorithms**: Exploring advanced methods (such as Spectral Clustering) and improving normalization/scaling.

---

**Thank you for your interest in the project!**
