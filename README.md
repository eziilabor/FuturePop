# FuturePop - Global Fertility Rate Prediction Project 🌍

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0+-orange.svg)](https://scikit-learn.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0+-yellow.svg)](https://tensorflow.org/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org/)

## Project Overview

This machine learning project predicts fertility rates for 150+ countries for 2024 using socio-economic indicators and demographic data from 2020-2023. By analyzing trends in Human Development Index (HDI), GDP per capita, female literacy, child mortality, and other key factors, we developed predictive models to forecast future demographic patterns.

## 🎯 Objectives

- Generate accurate fertility rate predictions for 2024 across global countries
- Compare performance between Random Forest and Neural Network models
- Identify key socio-economic factors influencing fertility trends
- Provide insights into future demographic changes worldwide

## 🛠️ Technologies Used

- **Python 3.8+**
- **Machine Learning**: Scikit-learn, TensorFlow/Keras
- **Data Processing**: Pandas
- **Visualization**: Topojson, D3
- **Model Evaluation**: StandardScaler, train-test split

## 📈 Models Implemented

### 1. Random Forest Regressor
- **Performance**: MAE: 0.225, MSE: 0.132, R²: 0.896
- **Features**: 100 estimators with standardized input features
- **Outcome**: Selected as the superior model

### 2. Neural Network (Keras)
- **Architecture**: One hidden layer (32 neurons) with ReLU activation
- **Performance**: MAE: 0.311, MSE: 0.183, R²: 0.855
- **Training**: 100 epochs with Adam optimizer

## 🔍 Key Features Used

- **HDI (Human Development Index)**
- **Previous Year Fertility Rate** (engineered feature)
- **Female Literacy Rate**
- **GDP Per Capita**
- **Child Mortality Rate**
- **Mean Age at First Birth**

## 📊 Data Processing

- **Time Period**: 2020-2023 training data
- **Countries**: 150+ nations with complete demographic data
- **Feature Engineering**: Created lagged fertility rate variable
- **Data Cleaning**: Handled missing values and applied StandardScaler normalization
- **Validation**: Used 2023 data for model testing and validation

## 🏆 Model Performance Comparison

| Model | MAE | MSE | R² Score |
|-------|-----|-----|----------|
| **Random Forest** | **0.225** | **0.132** | **0.896** |
| Neural Network | 0.311 | 0.183 | 0.855 |

*Random Forest demonstrated superior performance across all metrics*

## 📋 Project Structure

```
ML Models/
│
├── futurePop.ipynb              # Main analysis notebook
├── futurePopData.csv           # Training dataset (2020-2023)
├── predictionData.csv          # Actual 2024 data for validation
├── random_forest.csv           # Random Forest predictions
├── neural_network.csv          # Neural Network predictions
└── README.md                   # Project documentation
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas scikit-learn tensorflow numpy matplotlib
```

### Running the Analysis

1. Clone the repository
```bash
git clone https://github.com/eziilabor/FuturePop/tree/main
cd fertility-prediction
```

2. Run the Jupyter notebook
```bash
jupyter notebook futurePop.ipynb
```

## 🌐 Interactive Visualization

The project includes an **Interactive Real World Map** that displays:
- Predicted fertility rates by country
- Visual comparison between model predictions
- Demographic trend analysis
- Regional patterns and insights

*[Link to Interactive Map](https://webpages.charlotte.edu/kiyer6/futurePop/)*

## 📊 Key Insights

- **Strong Correlations**: HDI (-0.835) and female literacy (-0.784) show strong negative correlations with fertility rates
- **Economic Factors**: Higher GDP per capita generally correlates with lower fertility rates
- **Healthcare Impact**: Child mortality rates positively correlate (0.763) with fertility
- **Geographic Patterns**: Significant regional variations in fertility predictions

## 🔮 Future Enhancements

- [ ] Incorporate additional socio-economic indicators
- [ ] Implement time series forecasting for multi-year predictions
- [ ] Add uncertainty quantification to predictions
- [ ] Expand dataset to include more recent data
- [ ] Develop ensemble methods combining multiple models

## 📜 Data Sources

- World Bank demographic indicators
- UN Human Development Reports
- National statistical offices
- WHO health statistics

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:
- Model improvements
- Additional features
- Data quality enhancements
- Visualization updates

---

*This project demonstrates the application of machine learning techniques to demographic forecasting, providing valuable insights for policymakers, researchers, and organizations working in global development.*