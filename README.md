# 🩺 Diabetes Prediction using Machine Learning

This project predicts whether a patient is **Diabetic or Non-Diabetic** based on diagnostic health measurements.  
It uses multiple **Machine Learning algorithms** with **Hyperparameter Tuning** to achieve the best performance.  
A **Streamlit Web App** is also included so users can interact with the model.

---

## 📊 Dataset
The dataset used is the **Pima Indians Diabetes Dataset**, which contains the following features:

- Pregnancies  
- Glucose  
- BloodPressure  
- SkinThickness  
- Insulin  
- BMI  
- DiabetesPedigreeFunction  
- Age  
- **Outcome** (Target: 1 = Diabetic, 0 = Non-Diabetic)

---

## 🚀 Project Workflow
1. **EDA (Exploratory Data Analysis)**  
   - Distribution plots, correlations, histograms, boxplots.  
   - Key insights: Glucose, BMI, and Age strongly influence diabetes risk.

2. **Data Preprocessing**  
   - Handled missing/invalid values (replaced 0 with median).  
   - Standardized features using `StandardScaler`.  
   - Balanced dataset using **SMOTE**.

3. **Model Training & Evaluation**  
   - Algorithms tested:
     - Logistic Regression  
     - Naive Bayes  
     - KNN  
     - Random Forest  
     - Gradient Boosting  
     - SVM  
   - Used **GridSearchCV** for hyperparameter tuning.  
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC Curve.  

4. **Prediction Function**  
   - Takes patient data as input.  
   - Returns prediction + probability.

5. **Streamlit Web App**  
   - User-friendly interface to input patient data.  
   - Displays real-time prediction.  

---

## 🏆 Results
- Best models: **Random Forest** and **Gradient Boosting** (≈ 80–82% accuracy).  
- Logistic Regression provided a strong baseline (≈ 75%).  
- Important features: **Glucose**, **BMI**, **Age**.  

---

## ⚙️ Installation & Usage

### Clone the repository
```bash
git clone https://github.com/your-username/diabetes-prediction.git
cd diabetes-prediction
```

### Install dependencies
```bash
pip install -r requirements.txt
```

### Run Jupyter Notebook
```bash
jupyter notebook
```

### Run Streamlit App
```bash
streamlit run app.py
```

---

## 🖥️ Example Prediction
```python
sample = [[3, 124, 80, 33, 130, 33.2, 0.305, 26]]
sample_scaled = scaler.transform(sample)
prediction = best_model.predict(sample_scaled)
print("Prediction:", prediction[0])  # 0 = Non-Diabetic, 1 = Diabetic
```

---

## 📌 Future Improvements
- Deploy the Streamlit app to **Streamlit Cloud**.  
- Add **Explainability (SHAP values)**.  
- Integrate with a **database** for storing patient history.  

---

## 👨‍💻 Author
**Omar Husnye**  
- 💼 [LinkedIn](https://www.linkedin.com/)  
- 🐙 [GitHub](https://github.com/)
