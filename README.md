# Threat Actor Profiling - Machine Learning Based Intrusion Detection System

## Overview

Threat Actor Profiling is a machine learning-based cybersecurity project designed to detect and classify malicious network activities by analyzing network traffic patterns.

The system uses network flow features from the CICIDS2017 dataset to identify different types of cyber threats and classify traffic into attack categories. Multiple machine learning techniques were explored, with Random Forest achieving the highest accuracy of **99.48%** after model training and evaluation.

The project demonstrates the application of machine learning in intrusion detection, threat classification, and cybersecurity analytics.

---

## Objectives

- Detect malicious network traffic using machine learning techniques
- Classify different categories of cyber attacks
- Analyze network traffic patterns for threat identification
- Identify important features contributing to attack detection
- Generate threat actor profiles based on detected attack categories

---

## Features

- Combines multiple network traffic CSV files from the CICIDS2017 dataset
- Performs data preprocessing and cleaning
- Handles missing values and infinite values
- Performs feature engineering on network flow characteristics
- Converts attack labels into machine-readable categories
- Trains a machine learning classification model
- Evaluates model performance using classification metrics
- Generates confusion matrix visualization
- Extracts important network features influencing detection
- Maps detected attacks into threat actor profiles

---

## Dataset

**Dataset Used:**
CICIDS2017 - Canadian Institute for Cybersecurity Intrusion Detection Dataset

The dataset contains realistic network traffic data including:

- Benign traffic
- Denial of Service (DoS) attacks
- Distributed Denial of Service (DDoS) attacks
- Brute Force attacks
- Web attacks
- Port scanning activities
- Botnet traffic
- Other malicious network activities

---

## Technologies Used

### Programming Language
- Python

### Machine Learning Libraries
- Scikit-learn
- Pandas
- NumPy

### Data Visualization
- Matplotlib
- Seaborn

### Machine Learning Model

Implemented classification model:

- Random Forest Classifier

Model configuration:

```
n_estimators = 50
max_depth = 10
random_state = 42
```

---

## Workflow

```
Dataset Collection
        |
        ↓
Data Loading & Combining CSV Files
        |
        ↓
Data Cleaning & Preprocessing
        |
        ↓
Feature Engineering
        |
        ↓
Feature Scaling
        |
        ↓
Train-Test Split
        |
        ↓
Random Forest Model Training
        |
        ↓
Performance Evaluation
        |
        ↓
Threat Actor Profiling
```

---

## Data Processing

The following preprocessing steps were performed:

- Combined multiple CICIDS2017 CSV files
- Removed unnecessary features:
  - Flow ID
  - Source IP
  - Destination IP
  - Timestamp
- Handled missing and infinite values
- Encoded attack labels
- Applied feature scaling using StandardScaler

---

## Feature Engineering

Additional network behavior features were generated:

### Packets per Second

Measures packet transmission rate:

```
Total Forward Packets / Flow Duration
```

### Bytes per Second

Measures data transfer rate:

```
Total Forward Packet Length / Flow Duration
```

These features help identify abnormal network behavior patterns.

---

## Model Training

The dataset was divided into:

- Training Data: 80%
- Testing Data: 20%

The Random Forest classifier was trained using network flow features to classify different attack categories.

---

## Results

### Model Accuracy

```
Accuracy: 99.48%
```

### Classification Performance

The model achieved:

- High precision and recall for major attack categories
- Effective detection of benign and malicious traffic
- Strong classification performance across multiple threat categories

---

## Confusion Matrix

The confusion matrix was generated to visualize:

- Correct classifications
- Misclassified samples
- Model performance across different attack classes

(Add confusion matrix image here)

Example:

```
results/confusion_matrix.png
```

---

## Feature Importance Analysis

The Random Forest model was used to identify the most influential network traffic features.

Top features contributing to classification:

- Flow-related statistics
- Packet transmission characteristics
- Network traffic behavior patterns

(Add feature importance graph here)

---

## Threat Actor Profiling

The detected attack classes are mapped into security profiles:

| Detected Activity | Threat Profile |
|---|---|
| DoS/DDoS | High Traffic Flooding Attacker |
| Brute Force | Credential Attack Attempt |
| Port Scan | Reconnaissance Scanner |
| Bot Traffic | Automated Botnet Activity |
| XSS | Web Application Attacker |
| Benign Traffic | Normal User |

---

## Sample Output

Example:

```
Sample 1: Normal User
Sample 2: DoS Attacker (High Traffic Flooding)
Sample 3: Reconnaissance Scanner
```

---

## Future Improvements

- Implement additional machine learning models:
  - XGBoost
  - SVM
  - Neural Networks

- Perform real-time packet capture using:
  - Scapy
  - Wireshark integration

- Develop a dashboard for live threat monitoring

- Add deep learning-based intrusion detection

- Improve handling of imbalanced attack classes

---

## Project Structure

```
Threat-Actor-Profiling/
│
├── threat_actor_profiling.py
├── cicids2017.zip
├── README.md
├── requirements.txt
│
└── results/
    ├── confusion_matrix.png
    └── feature_importance.png
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/threat-actor-profiling.git
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the project:

```bash
python threat_actor_profiling.py
```

---

## Skills Demonstrated

- Machine Learning
- Network Intrusion Detection
- Cyber Threat Classification
- Data Preprocessing
- Feature Engineering
- Security Analytics
- Python Programming

---

## Author

**Parvathy S Ashok**

B.Tech Computer Science Engineering (Cyber Security)  
Amrita Vishwa Vidyapeetham
