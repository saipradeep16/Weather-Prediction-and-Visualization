# 🌦️ Weather Prediction and Visualization

## 📌 Introduction

This project focuses on predicting and visualizing various weather conditions such as drizzle, rain, sun, snow, and fog using the Seattle Weather Dataset. The objective is to explore historical patterns, validate hypotheses, and provide insights that help individuals and communities make informed weather-related decisions.

---

## 🎯 Motivation

Weather impacts everything from transportation and agriculture to public safety. Accurate forecasting can enhance planning and preparedness. This project uses data-driven techniques to understand temperature trends, precipitation levels, and how different weather types influence extreme conditions.

---

## 📊 Dataset Overview

- **Name**: Seattle Weather Prediction Dataset  
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/ananthr1/weather-prediction)  
- **Rows**: 1,461  
- **Columns**: 6  
- **Time Range**: 2012–2015  

### 📑 Features:
- `Date`: Timestamp  
- `Precipitation`: Rain/snow level (mm)  
- `Temp_max`: Maximum daily temperature (°C)  
- `Temp_min`: Minimum daily temperature (°C)  
- `Wind`: Wind speed (km/h)  
- `Weather`: Descriptive label (sunny, rainy, snowy, etc.)

---

## 🛠️ Tools & Libraries

- **Pandas** – Data manipulation  
- **NumPy** – Numerical computing  
- **Matplotlib** & **Seaborn** – Visualization  
- **Tableau** – Interactive dashboards  



## 📈 Exploratory Data Analysis (EDA)

### 1️⃣ Histogram – Max Temperature Distribution
```python
sns.histplot(weather_data['temp_max'], bins=30, kde=True)
```
Shows frequency of temperature values and outliers.

![Max Temp Histogram](images/chart_temp_max_hist.png)

---

### 2️⃣ Scatter Plot – Max Temperature vs Precipitation
```python
sns.scatterplot(x='temp_max', y='precipitation', data=weather_data)
```
Reveals relationship between heat and rainfall levels.

![Scatter Temp vs Precip](images/chart_scatter_temp_precip.png)

---

### 3️⃣ Line Chart – Temp Trends Over Time
```python
plt.plot(df['Date'], df['temp_max'], color='red')
plt.plot(df['Date'], df['temp_min'], color='blue')
```
Shows seasonal patterns and warming trend over 4 years.

![Line Chart](images/chart_temp_trends.png)

---

### 4️⃣ Correlation Heatmap – Weather Variables
```python
sns.heatmap(weather_data.corr(), annot=True, cmap='coolwarm')
```
Visualizes relationships between temp, wind, precipitation.

![Correlation Heatmap](images/chart_correlation_matrix.png)

---

## 🔍 Hypotheses Tested

### 📌 Hypothesis 1:
**Do certain weather types lead to extreme temperatures?**
```markdown
✅ Confirmed: Sunny conditions are associated with high temperatures; cold temps appear more in fog, snow, drizzle.
```
![Extreme Temp Chart](images/chart_extreme_weather_types.png)

---

### 📌 Hypothesis 2:
**Does temperature vary across the years?**
```markdown
✅ Confirmed: Clear increasing trend in both max and min temps from 2012 to 2015.
```
![Yearly Temp Trend](images/chart_yearly_temp_trend.png)

---

### 📌 Hypothesis 3:
**Do some weather categories show more precipitation?**
```markdown
✅ Confirmed: Rain and snow categories have significantly higher precipitation.
```
![Weather Precip Chart](images/chart_weather_vs_precip.png)

---

## ✅ Conclusion

This project revealed meaningful insights into how weather conditions relate to temperature and precipitation. We confirmed:

- Sunny weather is linked to high temps; rain/snow to lower temps  
- There is an upward temperature trend over the years  
- Rainy and snowy days carry higher precipitation loads  

Using Python, Seaborn, and Tableau, we built visual narratives and validated real-world assumptions. The findings emphasize the value of data visualization in environmental and public planning.

