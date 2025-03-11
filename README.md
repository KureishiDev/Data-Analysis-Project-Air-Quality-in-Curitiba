# Air Quality Analysis and Prediction

## Overview
This project aims to analyze air quality data and predict future trends using various machine learning and statistical models. It includes data collection, preprocessing, exploratory data analysis (EDA), time series forecasting, predictive modeling, and geographical visualization.

## Requirements
- pandas
- matplotlib
- seaborn
- folium
- geopandas
- scikit-learn
- statsmodels
- prophet

You can install all required packages with:
```bash
pip install pandas matplotlib seaborn folium geopandas scikit-learn statsmodels prophet
```

## Data
- `dados_qualidade_ar.csv`: Contains air quality measurements (e.g., PM2.5, PM10).
- `estacoes_monitoramento.csv`: Contains monitoring station information with their geographical coordinates.

## 1. Data Collection and Cleaning
- Loading datasets with pandas and performing basic cleaning operations such as handling missing values and formatting date columns.
- Example:
```python
dados_ar['data_hora'] = pd.to_datetime(dados_ar['data_hora'])
dados_ar.dropna(inplace=True)
```

## 2. Exploratory Data Analysis (EDA)
- Visualizing PM2.5 concentration over time using line plots.
- Displaying PM10 distribution by monitoring station with box plots.

## 3. Geographical Data Visualization
- Mapping monitoring stations using Folium and saving the map as an HTML file.
- Example:
```python
mapa_curitiba = folium.Map(location=[-25.4296, -49.2719], zoom_start=12)
```

## 4. Time Series Analysis (Prophet)
- Using Prophet to forecast PM2.5 levels for the next 30 hours.
- Example:
```python
model_prophet = Prophet()
model_prophet.fit(df_prophet)
forecast_prophet = model_prophet.predict(future)
```

## 5. Predictive Modeling (Linear Regression)
- Building a Linear Regression model to predict PM2.5 concentration based on features like temperature, humidity, and wind.
- Example:
```python
modelo = LinearRegression()
modelo.fit(X_train, y_train)
```

## 6. Visualizations
- Scatter plots to show relationships between variables (e.g., Temperature vs. PM2.5).

## Usage
Run the Python scripts to perform the analysis, visualize data, and generate predictions. Modify the CSV filenames and column names as needed to match your dataset.

## Future Improvements
- Incorporating more complex models (e.g., LSTM, ARIMA).
- Enhancing geographical visualizations with Folium.
- Extending analysis to multiple pollutants simultaneously.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

