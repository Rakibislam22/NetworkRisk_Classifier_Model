# Network Traffic Risk Classification System

## Project Overview

NetGuard AI is a machine learning-based system that classifies network traffic into three categories:

* ✅ Safe
* ⚠️ Suspicious
* ❌ Dangerous

The project uses the **Naive Bayes algorithm** on the **NSL-KDD dataset** to detect potential network threats based on traffic features.

---

## Objectives

* Analyze network traffic data
* Detect suspicious and dangerous activities
* Apply machine learning for cybersecurity classification
* Evaluate model performance using multiple metrics

---

## Dataset

* **Dataset Used:** NSL-KDD
* Contains network traffic records with multiple features
* Includes both normal and attack data

### Selected Features

* Duration
* Src Bytes
* Dst Bytes
* Count
* Same Service Rate
* Different Service Rate

---

## Methodology

### 1. Data Preprocessing

* Loaded dataset from `.txt/.csv`
* Added column names
* Removed unnecessary columns (e.g., difficulty)
* Selected important features

### 2. Label Simplification

Original labels converted into:

* `0 → Safe`
* `1 → Suspicious`
* `2 → Dangerous`

### 3. Feature Scaling

* Applied **StandardScaler** for normalization

### 4. Train-Test Split

* 80% Training
* 20% Testing

### 5. Model Training

* Used **Gaussian Naive Bayes**

---

## Model

* Algorithm: **Naive Bayes (GaussianNB)**
* Type: Classification Model

---

## Evaluation Metrics

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1 Score

---

## Visualizations

* Confusion Matrix (Seaborn Heatmap)
* Accuracy Graph (Learning Curve)
* Recall Graph
* F1 Score Graph
* Feature Scaling Comparison

---

## Example Prediction

```python
new_data = [[0, 200, 5000, 5, 1.0, 0.0]]
new_data_scaled = scaler.transform(new_data)
prediction = nb.predict(new_data_scaled)

labels = ["Safe", "Suspicious", "Dangerous"]
print(labels[prediction[0]])
```

---

## Technologies Used

* Python 🐍
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/Rakibislam22/NetworkRisk_Classifier_Model.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook or script:

```bash
python main.py
```

---

## Results

* Successfully classified network traffic
* Achieved good accuracy using a simple model
* Demonstrated effective intrusion detection

---

## Future Improvements

* Use advanced models (Neural Networks, Random Forest)
* Real-time network monitoring
* Deploy as a web application
* Add more features for higher accuracy

---

## Author

**Md Rakib Ali**

* GitHub: https://github.com/Rakibislam22
* GitHub: https://github.com/pranta2003

---

## Conclusion

This project demonstrates how machine learning can be used to detect network threats efficiently using simple yet powerful algorithms like Naive Bayes.

---

⭐ If you like this project, give it a star!
