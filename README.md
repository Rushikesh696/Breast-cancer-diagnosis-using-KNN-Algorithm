# Breast-cancer-diagnosis-using-KNN-Algorithm
### Problem Statement
Breast cancer is one of the leading causes of cancer-related deaths among women worldwide. Early diagnosis and classification of breast tumors into benign or malignant can significantly improve treatment outcomes. The dataset contains features computed from digitized images of fine needle aspirate (FNA) of breast masses.

### Objective
To build a classification model using the K-Nearest Neighbors (KNN) algorithm that can accurately predict whether a breast tumor is benign (non-cancerous) or malignant (cancerous) based on various cell nuclei features.

Dataset Overview
Total Entries: 569

Total Features: 33

Numerical Features: 30

ID Column: 1 (Dropped due to irrelevance)

Target Feature: diagnosis (B = benign, M = malignant)

Unnamed: 32 Column: Dropped due to being empty

Diagnosis Distribution:

Benign (B): 357 entries

Malignant (M): 212 entries

### Exploratory Data Analysis (EDA)
**✅ Data Quality Checks:**
No missing values in the dataset

No duplicate entries

All features are numerical except for diagnosis and id

**🧬 Feature Distributions:**
Features like radius_mean, texture_mean, perimeter_mean, smoothness_mean, symmetry_mean show normal distribution.

Features such as area_mean, compactness_mean, concavity_mean, concave points_mean, and fractal_dimension_mean are asymmetric.

Standard error and worst-case metrics (*_se, *_worst) are mostly right-skewed.

Boxplots reveal presence of outliers in almost all numerical features.

Pairplots suggest high inter-correlation between certain features.

**🔥 Correlation:**
Heatmap reveals strong positive correlations among radius_mean, perimeter_mean, area_mean, indicating potential for feature reduction via PCA or other techniques.

### Modeling Using K-Nearest Neighbors (KNN)
**✅ Preprocessing Steps:**
Converted target values: M → 1 and B → 0

Created a new target column and dropped the original diagnosis column

Dropped id and Unnamed: 32 as irrelevant

Split data into training (80%) and testing (20%)

Scaled features using StandardScaler to normalize the input space

**🧪 Model Training:**
Used KNeighborsClassifier with n_neighbors=9

Trained the model on scaled training data

**🎯 Model Performance:**
Achieved 96% accuracy on the test set

Model was validated using individual samples, successfully predicting both benign and malignant cases
