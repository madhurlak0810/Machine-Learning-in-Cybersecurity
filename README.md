# Machine Learning for Obfuscated Malware Detection

## Overview
This project explores the application of machine learning techniques to detect obfuscated malware within memory dumps. Given the increasing sophistication of malware that evades traditional detection methods, this study leverages modern machine learning algorithms to enhance cybersecurity defenses.

## Research Question
**How can machine learning techniques be effectively utilized to detect obfuscated malware within memory dumps?**  
The problem is approached as a binary classification task, distinguishing between benign and malicious memory dumps.

## Dataset
**CIC-MalMem-2022** dataset provided by the Canadian Institute for Cybersecurity:
- **Modality:** Memory dumps
- **Size:** 58,596 total records (50% benign, 50% malicious)
- **Features:** Engineered from memory dumps
- **Labels:** Binary (benign/malicious)
- **Collection Method:** Debug mode for memory dumping, simulating real-world scenarios
- **Malware Families:** Spyware, Ransomware, Trojan Horse, etc.

## Machine Learning Methodology
### 1. Feature Engineering
- Extracted relevant features from memory dumps.
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction and feature extraction.

### 2. Machine Learning Models
- **Traditional ML Algorithms:**
  - Random Forest (RF)
  - Support Vector Machines (SVM)
  - Logistic Regression
- **Deep Learning Models:**
  - Deep Neural Networks (DNN) with hyperparameter tuning

### 3. Dimensionality Reduction
- **PCA:** Used for feature extraction and noise reduction.
- **t-SNE & LDA:** Applied for visualization and maximizing class separability.

## Results
| Model              | Accuracy | Precision | Recall | F1 Score |
|--------------------|----------|-----------|--------|----------|
| **DNN MalwareDetector** | 99.77%  | 1.00      | 1.00   | 1.00     |
| Logistic Regression | 45.00%   | 0.45      | 0.48   | 0.47     |
| SVM                | 99.00%   | 0.99      | 0.99   | 0.99     |
| Random Forest      | 100.00%  | 1.00      | 1.00   | 1.00     |
| Gradient Boosting  | 100.00%  | 1.00      | 1.00   | 1.00     |

## Key Findings
- **Deep learning models (DNN) and ensemble methods (Random Forest, Gradient Boosting)** demonstrated superior performance.
- **Feature engineering and PCA** were crucial in enhancing detection efficiency.
- **Logistic Regression performed poorly**, indicating the complexity of the task.
- **Overfitting concerns:** The near-perfect results suggest the need for further validation on more diverse datasets.


