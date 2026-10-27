# Phishing Website Detection Using Machine Learning

## 📌 Project Overview

This project uses Machine Learning to detect phishing websites and distinguish them from legitimate websites. It uses the PhiUSIIL URL Dataset and a Linear Support Vector Machine (Linear SVM) classifier to analyze numerical website features and predict the class of a website.

Phishing websites are designed to trick users into revealing sensitive information, such as passwords and personal details. This project demonstrates how machine learning can help identify potentially malicious websites.

## 🎯 Objectives

- Detect phishing websites using machine learning.
- Analyze website features from a URL dataset.
- Preprocess data and handle missing or infinite values.
- Train a Linear SVM classification model.
- Evaluate the model using classification metrics and visualizations.

## 📂 Dataset

**Dataset name:** PhiUSIIL URL Dataset  
**File name:** `PhiUSIIL_URL_Dataset.csv`

The dataset contains website-related information and a `label` column used as the target variable.

The notebook removes selected text-based columns, including `URL`, `Domain`, `TLD`, and `Tile`, and uses numerical features for model training.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook

## ⚙️ Project Workflow

### 1. Data Loading
Load the CSV dataset using Pandas and inspect its shape, columns, and class distribution.

### 2. Data Preprocessing
- Remove records with missing target labels.
- Separate the target variable from the input features.
- Select numerical features.
- Replace infinite values with missing values.
- Fill missing feature values using the median.

### 3. Train-Test Split
Split the dataset into:
- **80% Training Data**
- **20% Testing Data**

The split uses `random_state=42` and stratification to preserve class proportions.

### 4. Model Training
Train a Linear Support Vector Machine (Linear SVM) using a Scikit-learn pipeline.

The pipeline includes:
- `StandardScaler` — scales numerical features.
- `LinearSVC` — classifies the input features.
- `class_weight="balanced"` — helps account for class imbalance.

### 5. Prediction
Use the trained model to predict labels for the test dataset.

### 6. Model Evaluation
Evaluate the model using:

- **Precision:** Measures how many predicted positive cases are actually positive.
- **Recall:** Measures how many actual positive cases are correctly identified.
- **F1 Score:** Combines precision and recall.
- **ROC-AUC:** Measures how well the model separates the two classes.
- **Confusion Matrix:** Displays correct and incorrect classifications.
- **Classification Report:** Summarizes classification performance.

### 7. Visualization
Generate a confusion matrix and ROC curve to visualize the model's performance.

## 📊 Expected Output

The notebook displays:

- Dataset information and class distribution.
- Training and testing sample counts.
- Actual and predicted labels.
- Confusion matrix.
- Precision, recall, F1 score, and ROC-AUC.
- Classification report.
- ROC curve.

Actual performance values depend on the dataset and execution results.

## ▶️ How to Run the Project

1. Download or obtain the `PhiUSIIL_URL_Dataset.csv` file.
2. Open `ML_.ipynb` in Google Colab or Jupyter Notebook.
3. Upload the dataset to your environment.
4. Update the dataset file path if necessary.
5. Run all notebook cells in order.
6. Review the model evaluation metrics and visualizations.

## 🔮 Future Enhancements

- Test additional classification algorithms.
- Perform feature selection and hyperparameter tuning.
- Develop a simple web interface for URL analysis.
- Integrate URL-based predictions into a website security tool.
- Evaluate the model on independent, real-world URL data.

## ⚠️ Disclaimer

This project is intended for educational and research purposes. Predictions should not be treated as a guarantee that a website is safe or malicious.

## 👩‍💻 Project Type

Machine Learning | Classification | Cybersecurity | Phishing Detection
