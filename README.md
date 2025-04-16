# Meteorological-Drought-Prediction-using-SSt
# **Meteorological Drought Prediction Using ML**  
**Predicting Drought in Jodhpur Using Sea Surface Temperatures (SSTs) & Machine Learning**  

---

## **📌 Project Overview**  
This project aims to predict **meteorological drought** in **Jodhpur, India**, using **Sea Surface Temperature (SST)** data and **Machine Learning (ML)** techniques.  

### **Key Objectives:**  
✔ Predict drought severity using **Standardized Precipitation Index (SPI)**  
✔ Analyze **SST anomalies** (Niño 3.4, Arabian Sea, Bay of Bengal)  
✔ Compare **ML models** (Logistic Regression, LSTM, XGBoost, N-BEATS)  
✔ Provide early warnings for **agriculture & water management**  

---

## **📂 Dataset**  
### **1. Rainfall Data (1901–2023)**  
- **Source:** India-WRIS, Jodhpur regional offices  
- **Processing:**  
  - Aggregated daily → monthly rainfall  
  - Calculated **SPI (Standardized Precipitation Index)**  
  - Classified drought severity (Moderate, Severe, Extreme)  

### **2. Sea Surface Temperature (SST) Data**  
- **Regions:** Niño 3.4, Arabian Sea, Bay of Bengal  
- **Sources:**  
  - NOAA ERDDAP ([link](https://coastwatch.pfeg.noaa.gov/erddap/griddap/erdHadSST.html))  
  - India-WRIS ([link](https://indiawris.gov.in/wris/#/timeseriesdata))  

---

## **⚙️ Methodology**  
### **1. Data Preprocessing**  
- **Merged SST & rainfall data**  
- **Lag feature engineering** (2–3 months for SST impact)  
- **Normalization & missing value handling**  

### **2. Models Implemented**  
| Model | Type | Key Features | Best Metric |
|-------|------|-------------|-------------|
| **Logistic Regression** | Classification | Baseline model | **Accuracy: 64%** |
| **LSTM** | Deep Learning (Time Series) | Sequential pattern learning | **R²: 0.60, RMSE: 0.98** |
| **XGBoost** | Ensemble Learning | Handles non-linear relationships | **R²: 0.96, RMSE: 0.0358** |
| **N-BEATS** | Neural Forecasting | Interpretable time-series model | **MAE: 0.12, RMSE: 0.15** |

### **3. Evaluation Metrics**  
| Metric | Full Form | Use Case | Ideal Value |
|--------|-----------|----------|------------|
| **RMSE** | Root Mean Squared Error | Regression error | **Lower = Better** |
| **MAE** | Mean Absolute Error | Robust error measure | **Lower = Better** |
| **R²** | R-Squared | Variance explained | **Closer to 1 = Better** |
| **F1-Score** | Precision-Recall Balance | Classification | **Higher = Better** |

---

## **📊 Key Results**  
### **1. Logistic Regression**  
- **Accuracy:** 64%  
- **Key Insight:** SST lags (2–3 months) strongly influence Jodhpur’s droughts.  

### **2. LSTM (Long Short-Term Memory)**  
- **R²:** 0.60  
- **Best at:** Capturing **temporal dependencies** in rainfall patterns.  

### **3. XGBoost**  
- **R²:** **0.96** (Best performing)  
- **Low RMSE (0.0358)** → Highly accurate SPI predictions.  

### **4. N-BEATS (Neural Forecasting)**  
- **MAE: 0.12** → Smooth & stable drought forecasts.  
- **Interpretable** trend analysis.  

---

## **📂 Repository Structure**  
```
📦Drought-Prediction-ML  
├── 📂Data  
│   ├── Rainfall_Jodhpur.csv  
│   ├── SST_Regions.csv  
│   └── Processed_SPI.csv  
├── 📂Notebooks  
│   ├── 1_Data_Preprocessing.ipynb  
│   ├── 2_Logistic_Regression.ipynb  
│   ├── 3_LSTM_Model.ipynb  
│   ├── 4_XGBoost.ipynb  
│   └── 5_NBEATS_Forecasting.ipynb  
├── 📂Models  
│   ├── logistic_model.pkl  
│   ├── lstm_model.h5  
│   └── xgboost_model.json  
├── 📜README.md  
└── 📜requirements.txt  
```

---

## **🚀 How to Run?**  
1. **Clone the repo:**  
   ```bash
   git clone https://github.com/your-username/Drought-Prediction-ML.git
   cd Drought-Prediction-ML
   ```
2. **Install dependencies:**  
   ```bash
   pip install -r requirements.txt
   ```
3. **Run Jupyter notebooks:**  
   ```bash
   jupyter notebook
   ```

---


---

## **📜 License**  
MIT License  

---

## **🔗 References**  
- [NOAA SST Data](https://coastwatch.pfeg.noaa.gov/erddap/griddap/erdHadSST.html)  
- [India-WRIS Rainfall Data](https://indiawris.gov.in/wris/#/timeseriesdata)  

---

**🌧️ Predicting Droughts Before They Strike!**  
*For queries, contact: [manasdwivedi2004@gmail.com]*
