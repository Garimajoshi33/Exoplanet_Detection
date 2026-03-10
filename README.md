# 🌌 Exoplanet Analyzer
## Detecting Exoplanets using Machine Learning and Stellar Light Curve Analysis

This project builds a **machine learning pipeline to detect exoplanets from stellar brightness data**. The system analyzes **light curves (flux measurements)** of stars and predicts whether a star system contains an exoplanet.

The dataset used in this project is derived from observations made by the **Kepler Space Telescope**, which detects planets using the **transit method** — observing small dips in a star's brightness when a planet passes in front of it.
---

## 🛰️ How Exoplanet Detection Works

The **transit method** is one of the most widely used techniques for detecting exoplanets.

When a planet passes in front of its host star:

1. The star's brightness **drops slightly**
2. This drop creates a **dip in the light curve**
3. Repeated dips indicate a **possible orbiting planet**

Machine learning models can learn these patterns from large datasets of stellar brightness measurements.

---

## 📂 Project Structure

```
Exoplanet-Detector
│
├── data
│   ├── raw
│   │   ├── exoTrain.csv
│   │   └── exoTest.csv
│   │
│   └── processed
│
├── notebooks
│   └── data_exploration.ipynb
│
├── src
│
├── models
│   ├── exoplanet_classifier.pkl
│   └── scaler.pkl
│
├── requirements.txt
└── README.md
```

---

## 📊 Dataset Information

The dataset contains **stellar brightness measurements** collected from thousands of stars.

### Dataset Files

* **exoTrain.csv** → Training dataset  
* **exoTest.csv** → Testing dataset  

### Dataset Structure

Each row represents **one star system**.

* **LABEL** → Indicates presence of an exoplanet  
* **FLUX.1 – FLUX.3197** → Brightness measurements over time

### Label Meaning

* **1 → Exoplanet detected**
* **2 → No exoplanet**

For machine learning, these labels are converted to:

* **1 → Exoplanet**
* **0 → No Exoplanet**

---

## ⚙️ Technologies Used

### Programming Language

* **Python**

### Libraries

* **Pandas** → Data analysis
* **NumPy** → Numerical computations
* **Matplotlib** → Data visualization
* **Seaborn** → Statistical visualization
* **Scikit-learn** → Machine learning algorithms
* **Imbalanced-learn** → Handling class imbalance (SMOTE)

---

## 🧠 Machine Learning Pipeline

The following steps were performed in the project:

### 1️⃣ Data Loading
Load training and testing datasets.

### 2️⃣ Exploratory Data Analysis
Understand dataset structure and visualize stellar light curves.

### 3️⃣ Label Transformation
Convert labels into binary format for classification.

### 4️⃣ Feature Scaling
Normalize brightness values using **StandardScaler**.

### 5️⃣ Handling Class Imbalance
Apply **SMOTE (Synthetic Minority Oversampling Technique)** to balance the dataset.

### 6️⃣ Model Training
Train a **Random Forest Classifier** for exoplanet detection.

### 7️⃣ Model Evaluation
Evaluate model performance using:

* **Accuracy Score**
* **Confusion Matrix**
* **Classification Report**

### 8️⃣ Feature Importance Analysis
Identify which brightness measurements contribute most to predictions.

### 9️⃣ Model Saving
Save the trained model and scaler using **pickle**.

---

## 📈 Model Performance

The trained model demonstrates strong performance in identifying exoplanets.

Evaluation metrics used include:

* **Accuracy**
* **Precision**
* **Recall**
* **F1 Score**
* **Confusion Matrix**

These metrics help determine how well the model detects **planetary transit signals** in stellar light curves.

---

## 📊 Visualizations

The project includes several visual analyses:

* **Stellar Light Curve Graphs**
* **Confusion Matrix Heatmap**
* **Feature Importance Plot**

These help understand how the model detects exoplanets from brightness patterns.

---

## 💾 Saved Models

The trained artifacts are stored in the **models** directory.

* **exoplanet_classifier.pkl** → Trained Random Forest model
* **scaler.pkl** → StandardScaler used for feature scaling

These allow predictions on new data **without retraining the model**.

---

## 👩‍💻 Author

**Garima Joshi**

Machine Learning & Data Science Enthusiast

---

⭐ If you found this project useful, consider **starring the repository**.
