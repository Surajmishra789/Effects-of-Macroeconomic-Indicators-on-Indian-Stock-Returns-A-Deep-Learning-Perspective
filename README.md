# Effects of Macroeconomic Indicators on Indian Stock Returns: A Deep Learning Perspective  

## Overview  
This project investigates the relationship between key macroeconomic indicators and Indian stock market performance using advanced machine learning and deep learning techniques.  
It analyzes how variables such as GDP, inflation, repo rate, exchange rate, and foreign institutional investment (FII) influence stock indices like NIFTY 50 and SENSEX, and evaluates multiple predictive models to identify the most effective approach.

## Problem Statement  
Existing studies often examine macroeconomic indicators and stock market prediction separately. Additionally, many approaches use improper validation techniques and limited evaluation metrics.  
This project addresses whether deep learning models can outperform traditional econometric and machine learning models in forecasting macroeconomic trends and stock market behavior using long-term time-series data.

## Objectives  
- Analyze relationships between macroeconomic indicators and stock market performance  
- Develop forecasting models using econometric, machine learning, and deep learning approaches  
- Compare models using multiple evaluation metrics  
- Identify the most effective predictive model  
- Provide insights for financial decision-making  

## Dataset  
- **Time Period:** 2004 – 2025 (Quarterly)  
- **Observations:** 87  

### Features  
- GDP  
- Inflation (CPI/WPI)  
- Repo Rate  
- Exchange Rate (INR/USD)  
- FII (Equity, Debt, Total)  
- NIFTY 50 High  
- SENSEX High  

## Methodology  
### Data Preprocessing  
- Missing values handled using forward-fill interpolation  
- Min-Max normalization applied to features and target  
- Pearson correlation analysis performed  

### Sequence Construction  
- Sliding window approach (4 quarters)  
- Generated 83 sequence-target pairs  

### Train-Test Split  
- 80% training and 20% testing  
- Chronological split (no shuffling) to preserve temporal order
  
## Models Implemented  

### Econometric Models  
- ARIMA  
- VAR  

### Machine Learning Models  
- Random Forest  
- XGBoost  
- Support Vector Machine (SVM)  

### Deep Learning Models  
- LSTM (Long Short-Term Memory)  
- GRU (Gated Recurrent Unit)  
- TCN (Temporal Convolutional Network)  

## Evaluation Metrics  
- **RMSE:** Measures prediction error magnitude  
- **R² Score:** Measures model fit  
- **MAPE:** Percentage-based error  
- **Directional Accuracy:** Measures trend prediction (up/down)  
- **AUC:** Measures classification performance for direction  

---

## 📊 Results  

| Model         | Performance Summary      |
|-------------- |--------------------------|    
| **GRU**       | Best overall performance |
| LSTM          | Strong performance       |
| ARIMA         | Limited performance      |
| XGBoost       | Poor generalization      |
| Random Forest | Stable but less accurate |
| SVM           | Weak performance         |
| TCN           | Underperformed           |

### Key Findings  
- GRU achieved the lowest RMSE, highest R², and lowest MAPE  
- Achieved **75% directional accuracy**  
- Deep learning models significantly outperform traditional approaches
  
## Key Insights  
- Macroeconomic indicators strongly influence stock market behavior  
- Deep learning models effectively capture nonlinear and temporal patterns  
- Proper time-series validation is critical for realistic evaluation  

## Limitations  
- Limited dataset size (87 observations)  
- External shocks (e.g., COVID-19, global crises) not explicitly modeled  
- No sentiment or behavioral data included  

## Future Work  
- Incorporate high-frequency data (monthly/weekly)  
- Integrate sentiment analysis (news/social media)  
- Develop hybrid models (DL + econometric)  
- Improve model interpretability  

## Tech Stack  
- Python  
- TensorFlow / Keras  
- Scikit-learn  
- XGBoost  
- Statsmodels  
- Pandas, NumPy  
- Matplotlib, Seaborn  
