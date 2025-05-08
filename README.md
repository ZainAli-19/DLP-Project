# DLP Project - Solar Energy Forecasting  
**Roll No:** 21K-4870  
**Section:** BCS-DLP 8B  

## 📘 Project Title  
**Deep Learning-Based Forecasting of Solar Energy Generation Using Weather Data**

---

## 🧠 Project Description  
This project aims to forecast solar energy output using deep learning models trained on hourly weather and solar generation data. The models compared include:  
- **LSTM (Long Short-Term Memory)**
- **GRU (Gated Recurrent Unit)**
- **Transformer Encoder**

All models predict hourly solar output using the past 24 hours of weather and system data.

---

## 🗃️ Dataset  
- **Solar Generation**: Hourly kWh values (2022–2024) from multiple solar sites  
- **Weather Data**: Hourly temperature, humidity, wind speed, etc.  
- **Merged on**: `Year`, `Month`, `Hour`

---

## 🧪 Models Overview

| Model       | MAE     | RMSE     | R²     | MAPE (%)     |
|-------------|---------|----------|--------|--------------|
| **LSTM**     | 16,868  | 29,633   | 0.3672 | 4.81         |
| **GRU**      | 11,296  | 19,406   | 0.7286 | 465.37       |
| **Transformer** | 20,191  | 30,871   | 0.3132 | 1,515.82     |

- **Best R² and RMSE**: GRU  
- **Most stable MAPE**: LSTM  
- **Transformer** suffered from MAPE distortion due to zero or low actual values.

---

## 🧰 Tools & Libraries  
- Python 3.11  
- TensorFlow / Keras  
- Scikit-learn  
- Pandas / NumPy  
- Matplotlib  
- Google Colab (12 GB RAM, TPU runtime)

---

## ⚙️ Technical Details  
- Input: Sliding window of 24-hour sequences  
- Normalization: `MinMaxScaler`  
- Optimizer: `Adam`  
- Loss: `Mean Squared Error`  
- Learning Rate Scheduler: `ReduceLROnPlateau`  
- EarlyStopping (GRU and Transformer)

---

## 📂 Files Included  
- `DLP_Report.pdf` – Final formatted scientific report  
- `README.md` – This file  
- Source code (optional: include notebooks or `.py` scripts)

---

## 📈 Future Improvements  
- Handle low-output periods to stabilize MAPE  
- Incorporate external factors (holidays, sunlight hours)  
- Tune Transformer further with positional embeddings  
- Try hybrid CNN-RNN architectures

---

## ✍️ Author  
**Name:** Zain Ali Siddiqui  
**Roll No:** 21K-4870  
**Course:** Deep Learning Project (BCS-DLP 8B)  
