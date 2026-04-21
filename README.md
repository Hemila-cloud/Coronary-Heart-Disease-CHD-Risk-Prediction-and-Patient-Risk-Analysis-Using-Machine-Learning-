# Coronary Heart Disease (CHD) Prediction and Risk Segmentation using Machine Learning



## Project Overview
Coronary Heart Disease (CHD) is one of the leading causes of mortality worldwide. Early prediction of individuals at risk is critical for reducing complications and improving healthcare outcomes.

This project develops a **machine learning-based predictive framework** to estimate the likelihood of CHD occurrence within a 10-year period using clinical, behavioural, and demographic data. In addition to prediction, the project performs **patient segmentation using clustering techniques** to identify distinct risk groups and derive actionable healthcare insights.



## Objectives
- Predict the probability of CHD occurrence (binary classification)
- Handle **class imbalance using SMOTE**
- Identify key **risk factors influencing CHD**
- Segment patients into **risk groups using K-Means clustering**
- Provide actionable insights for:
  - Healthcare practitioners
  - Insurance companies
  - Public health agencies



## Key Features of the Project
- Use of **balanced dataset (SMOTE)** for improved learning
- Comparison of **Logistic Regression and Random Forest models**
- Application of **feature scaling for model stability**
- Detection and treatment of **outliers using IQR method**
- Integration of **unsupervised learning (K-Means clustering)**



## Dataset
- **Source:** Framingham Heart Study Dataset
- **Total Records:** 7,192 (original)
- **Training Records (after SMOTE):** 5,754
- **Features:** 16 (15 predictors + 1 target)

###  Key Features Include:
- Demographic: Age, Gender, Education
- Behavioural: Smoking status, Cigarettes per day
- Medical History: Hypertension, Diabetes, Stroke
- Physiological: Blood Pressure, Cholesterol, Glucose, BMI, Heart Rate

###  Target Variable:
- **TenYearCHD**
  - 1 → Likely to develop CHD
  - 0 → Not likely



## Workflow

###  Data Preprocessing
- Handled missing values:
  - Median imputation (continuous variables)
  - Mode imputation (categorical variables)
- Outlier treatment using **IQR-based capping (winsorization)**
- Standardized features using **StandardScaler**
- Verified zero missing values



###  Handling Class Imbalance
- Applied **SMOTE (Synthetic Minority Oversampling Technique)**
- Achieved balanced dataset:
  - 50% CHD
  - 50% Non-CHD



###  Exploratory Data Analysis (EDA)

#### Univariate Analysis
- Distribution of continuous features (age, BMI, glucose, etc.)
- Bar plots for categorical variables

####  Bivariate Analysis
- Continuous features vs CHD (boxplots, violin plots)
- Categorical features vs CHD (percentage comparisons)

####  Key Insights:
- Age and systolic BP strongly influence CHD risk
- Smoking and glucose levels show positive association
- Hypertension is a major risk factor



###  Model Building

#### Logistic Regression
- Baseline model
- Suitable for interpretability

####  Random Forest (Best Model)
- Captures non-linear relationships
- Handles feature interactions effectively



###  Model Evaluation

Metrics used:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

###  Best Model Performance (Random Forest)
- Accuracy: **91.3%**
- Precision: **96.8%**
- Recall: **85.3%**
- ROC-AUC: **97.6%**



###  Clustering (Risk Segmentation)

- Applied **K-Means clustering**
- Segmented patients into:
  - Low-risk group
  - Medium-risk group
  - High-risk group



###  Insights & Interpretation

- High-risk patients tend to have:
  - Higher age
  - Elevated blood pressure
  - Higher glucose levels
  - Smoking habits

- Hypertension and diabetes significantly increase CHD risk



##  Visualizations
- Dataset statistical summary
- Histograms for continuous variables
- Bar charts for categorical features
- Boxplots (feature vs CHD)
- Violin plots for distribution comparison
- Correlation analysis
- Cluster visualization



## Output
- Trained classification models
- Predicted CHD probabilities
- Risk-segmented patient groups
- Feature importance insights



##  Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib, Seaborn



## Conclusion
This project demonstrates that machine learning models, particularly **Random Forest**, can effectively predict CHD risk using structured healthcare data. The integration of **SMOTE, feature scaling, and clustering** enhances both predictive performance and interpretability, enabling better decision-making in healthcare systems.



## Future Work
- Incorporate deep learning models for improved prediction
- Use longitudinal patient data for time-series analysis
- Deploy as a real-time clinical decision support system
- Integrate with hospital databases for live monitoring

