# 🧠 Employee Attrition Analysis

Analisis prediksi employee attrition menggunakan machine learning. 
Tujuan dari project adalah:
- Menganalisis faktor-faktor yang mempengaruhi employee attrition.
- Membangun dan mengevaluasi model prediksi karyawan yang berisiko resign.
- Memberikan rekomendasi berbasis data untuk mendukung strategi retensi SDM.

## 📂 Dataset

Dataset yang digunakan adalah dataset HR Analytics Employee Attrition

- Jumlah data: 1470 rows dan 35 columns
- Target: `Attrition` (Yes / No)

## 📊 Exploratory Data Analysis (EDA)

Beberapa insight yang ditemukan dari data:
- Karyawan yang bekerja lembur (*OverTime*) cenderung lebih sering mengundurkan diri.
- Karyawan dengan penghasilan lebih tinggi cenderung bertahan.
- Karyawan yang lebih muda lebih banyak mengalami attrition.
- Karyawan yang keluar cenderung memiliki jarak rumah ke kantor yang lebih jauh.
  
---

## ⚙️ Preprocessing

Langkah-langkah preprocessing:
- Handling missing values
- Encoding kategorikal
- Feature scaling dengan `StandardScaler`
- Penanganan imbalance data menggunakan **SMOTE**

---

## 🤖 Modeling

Tiga model yang digunakan:
- ✅ Logistic Regression
- ✅ Random Forest
- ✅ XGBoost

Model terbaik dipilih berdasarkan **generalization performance** (evaluasi di test set).

---

## 🧪 Evaluation

| Model              | Accuracy | Recall | Precision | F1 Score | ROC AUC | Overfitting |
|-------------------|----------|--------|-----------|----------|---------|-------------|
| Logistic Regression | 0.77     | **0.79** | 0.39      | **0.52** | 0.8060  | ❌ Stabil    |
| Random Forest      | 0.85     | 0.28   | **0.54**  | 0.37     | 0.7998  | ✅ Overfitting |
| XGBoost            | 0.84     | 0.28   | 0.52      | 0.36     | 0.8111  | ✅ Overfitting |

➡️ **Model Terbaik:** Logistic Regression  
✔️ Generalisasi baik  
✔️ Recall tinggi  
✔️ F1 score seimbang

---

## 🔍 Feature Importance (Top 10)

Fitur paling berpengaruh menurut **Logistic Regression**:
1. OverTime
2. TotalWorkingYears
3. YearsSinceLastPromotion
4. NumCompaniesWorked
5. YearsWithCurrManager
6. EnvironmentSatisfaction
7. Department
8. JobSatisfaction
9. Age
10. MaritalStatus

---

## 🚀 Kesimpulan

Model terbaik adalah **Logistic Regression**, karena:
- Tidak overfitting
- Recall tinggi (baik untuk mendeteksi risiko keluar)
- F1 Score seimbang
- Lebih mudah diinterpretasi

---

## 📦 Cara Menjalankan

```bash
# Clone repo
git clone https://github.com/monalisa0603/Employee-Attrition-Analysis.git
cd Employee-Attrition-Analysis

# Jalankan di Jupyter/Colab
