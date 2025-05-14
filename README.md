# itds_final_project

# 📊 Regression Techniques: From Function Approximation to Time Series Forecasting

This project explores a variety of regression techniques, from simple univariate analytical functions to complex multivariate datasets and time series forecasting. Implemented using `scikit-learn`, `numpy`, `pandas`, and `matplotlib`, this study is divided into three main exercises:

---

## 📘 Exercise 1: Function Approximation

### Objective
Approximate three analytical functions using regression models:

1. `f1(x) = x · sin(x) + 2x`
2. `f2(x) = 10 · sin(x) + x²`
3. `f3(x) = sign(x)(x² + 300) + 20 · sin(x)`

### Steps
- Generated synthetic dataset using `numpy`.
- Applied and evaluated multiple regression models:
  - Linear Regression
  - Polynomial Regression (degree 5)
  - Support Vector Regression (RBF Kernel)
  - Random Forest Regressor
  - MLP Regressor

### Feature Engineering
- Introduced new features like `sin(x)`, `cos(x)`, and `x²` to capture function shapes better.
- Random Forest with engineered features showed the best performance:

---

## 📘 Exercise 2: Multivariate Regression

### Objective
Model the relationship between multiple features and a target variable, simulating a real-world scenario like predicting car prices.

### Steps
- Created synthetic dataset using `make_regression` with 2000 samples.
- Evaluated performance with and without added noise and non-informative features.
- Analyzed feature importance using Linear Regression coefficients.

### Key Observations
- Linear regression performed well on clean data (R² ≈ 0.999).
- Performance decreased with added noise and non-informative features (R² ≈ 0.978).
- Coefficients close to zero indicated non-informative features.

---

## 📘 Exercise 3: Time Series Forecasting – WWII Weather Dataset

### Objective
Predict daily mean temperatures using historical weather data from sensor `STA = 22508`.

### Dataset
- Loaded from `Summary of Weather.csv`
- Filtered for sensor `22508`
- Target: `MeanTemp`

### Preprocessing
- Created rolling window dataset to predict next day’s temperature.
- Trained on 1940–1944 data, tested on 1945 data.
- Considered scaling and normalization techniques.

### Models Evaluated
- Linear Regression
- Random Forest Regressor
- MLP Regressor

### Results
- Random Forest performed best.
- Seasonality and trend were captured reasonably well.
- Predicting longer horizons would require:
- Recurrent models (e.g., LSTM)
- Sequence-to-sequence models
- Exogenous variable incorporation

### Visualization
Plotted predicted vs actual temperatures:
- Observed alignment in trend and seasonal fluctuations
- Identified areas where the model lagged in extremes

---

## ⚙️ Technologies Used

- Python 3.x
- pandas
- numpy
- matplotlib
- scikit-learn

---

## 📈 Metrics Used

- `Mean Squared Error (MSE)`
- `R² Score (Coefficient of Determination)`

---

## ✅ How to Run

1. Clone the repository
2. Ensure dependencies are installed
3. Add source csv to root
4. Run notebook

---

## 💡 Lessons Learned

- Simple linear models work well with clean, well-structured data.
- Feature engineering can significantly boost performance.
- Time series forecasting requires careful preprocessing (e.g., rolling windows, temporal splits).
- Visualization is key to understanding regression quality.

---

## 📁 Dataset Sources

- WWII Weather Dataset: https://github.com/dbdmg/data-science-lab/raw/master/datasets/weatherww2.zip
---

## 📁 GitHub

- GitHub repository: https://github.com/kelenbailey/itds_final_project.git
---

