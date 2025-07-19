#  AI-Based Air Quality Prediction

## Project Overview

This project aims to **predict NO₂ air pollution levels** using **machine learning models** trained on historical **air quality and weather data**. The focus is on **Beijing-like urban environments**, where rising pollution poses serious health risks.

Using AI models, city planners and authorities can anticipate pollution levels and take **preventive actions** to safeguard public health.

---

## Dataset Description

- **Dataset Name:** AirQuality.csv  
- **Source:** UCI Machine Learning Repository  
- **Size:** ~9,358 records  
- **Features:**  
  - Pollutant concentrations: `CO(GT)`, `NO2(GT)`, `C6H6(GT)`  
  - Weather data: `T` (temperature), `RH` (humidity), `AH` (absolute humidity)  
  - Time and date fields

- **Target Variable:**  
  `NO2(GT)` – Nitrogen Dioxide level (proxy for air pollution)

---

## Methodology

### Approach
1. **Data Preprocessing**
   - Replaced missing values (`-200`) with NaN
   - Converted European-style numbers (`2,6`) to decimal (`2.6`)
   - Removed rows with missing key features
2. **Feature Selection**
   - Used: `CO(GT)`, `T`, `RH`, `AH`
   - Target: `NO2(GT)`
3. **Scaling**
   - Used `StandardScaler` for normalization
4. **Train-Test Split**
   - 80% training, 20% testing
5. **Model Training**
   - Trained three regression models
6. **Model Evaluation**
   - Evaluated with R² Score, MAE, RMSE

### Algorithms Used
- **Linear Regression** – Baseline model  
- **Decision Tree Regressor** – Captures non-linear relationships  
- **Random Forest Regressor** – Ensemble for better performance

---

## 📊 Results

| Model                | R² Score | MAE    | RMSE   |
|---------------------|----------|--------|--------|
| Linear Regression   | ~0.42    | ~22.4  | ~29.6  |
| Decision Tree       | ~0.60    | ~18.2  | ~25.3  |
| Random Forest       | **~0.70**| **14.9**| **21.5** |

**Random Forest performed the best**, offering accurate and robust predictions.

---

## 📈 Visualizations

- **Actual vs Predicted Plot** for Random Forest
- **Feature importance** to understand model insights

---

## Future Work

- Incorporate more external data (e.g., traffic, industrial zones)
- Apply deep learning (LSTM) for time-series forecasting
- Build a live dashboard to monitor air quality in real time
- Extend predictions to PM2.5, O₃, and SO₂

---

## How to Run
1. Upload `AirQuality.csv` to your Colab or local directory
2. Install dependencies:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn

## Project link
https://github.com/HarshitaY04/AQI.git
