# Human Activity Recognition using Sensor Data 📊

This project focuses on classifying human activities based on time-series data collected from wearable sensors. We used various statistical methods, feature engineering techniques, and deep learning models to enhance performance and interpretability.

## 📂 Dataset Overview
- **Data Type:** Tabular, time-series measurements  
- **Sensors:** Smartwatch, Vicon  
- **Users:** Data collected from 8 train users, 21 test users  
- **Activities:** 18 unique activities (e.g., walking, stairs down, using phone)  
- **Samples:**  
  - Train: 50,248 rows  
  - Test: 74,744 rows  
- **Class Imbalance:** Frequent activities like "walking freely" and "using phone" dominate the dataset  

## 🛠️ Approach & Methodology
1. **Exploratory Data Analysis:**  
   - Analyzed activity distribution and sensor readings  
   - Identified significant class imbalance and varying sequence lengths  

2. **Feature Engineering:**  
   - Extracted statistical features like mean, variance, and skewness  
   - Applied normalization methods (StandardScaler, MinMaxScaler)  
   - Dimensionality reduction using PCA  

3. **Modeling:**  
   - **Naive Baselines:**  
     - Most Common Label  
     - Last Observation Carried Forward  
   - **Traditional ML:**  
     - Random Forest  
   - **Deep Learning Models:**  
     - 1D-CNN  
     - LSTM  
     - Multi-Layer Perceptron (MLP)  

4. **Training Strategy:**  
   - Split dataset by sensor type (Smartwatch, Vicon) for specialized models  
   - Allocated 20% of data for validation, maintaining representative distribution  

## 📊 Results
| Model         | Sensor     | Accuracy  | Correct Predictions | Incorrect Predictions |
|---------------|------------|-----------|---------------------|-----------------------|
| 1D-CNN        | Smartwatch | 83.00%    | 5994                 | 1235                  |
| 1D-CNN        | Vicon      | 33.00%    | 922                  | 1886                  |
| LSTM          | Smartwatch | 85.07%    | 6150                 | 1079                  |
| LSTM          | Vicon      | 31.20%    | 876                  | 1932                  |

## 🚀 Key Takeaways
- **Best Model:** LSTM on Smartwatch data with **85.07% Accuracy**  
- **Challenges:**  
  - Class imbalance and similar activity patterns  
  - Varying data quality between sensor types  
- **Solutions Applied:**  
  - Feature Importance and Dimensionality Reduction  
  - Normalization and Data Augmentation  
  - Specialized models per sensor type  

## 🔍 Future Improvements
- Fine-tuning hyperparameters and exploring attention mechanisms  
- Implementing ensemble methods for combining model predictions  
- Addressing sensor discrepancies with domain adaptation techniques  

## 📝 Authors
- Eyal Shubeli
- Nadav Toledo  

