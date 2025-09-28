# 🔌 Household Power Consumption Analysis

This project provides a comprehensive analysis of the **Household Power Consumption Dataset**, focusing on energy usage patterns across various time scales (hourly, daily, and monthly). The workflow includes **data cleaning, preprocessing, exploratory data analysis (EDA), correlation studies, and trend visualizations** to derive actionable insights into household electricity consumption.

---

## 📂 Dataset Overview

| Attribute              | Description                                      |
|------------------------|--------------------------------------------------|
| Records                | `df.shape` → Total number of rows & columns      |
| Missing Values         | Checked using `df.isnull().sum()`                |
| Data Types             | Verified with `df.info()`                        |
| Date Range             | From `df['Date'].min()` to `df['Date'].max()`    |
| Sub-metering Columns   | `Sub_metering_1`, `Sub_metering_2`, `Sub_metering_3` |

---

## 🧹 Data Cleaning & Preparation

- Replaced `"?"` with `NaN` in power and sub-metering columns  
- Converted data types to **float**  
- Filled missing values with **0**  
- Created a new column for total sub-metering:
- Converted `Date` and `Time` to **DateTime** format  
- Extracted **Hour, Day, and Month** features for temporal analysis  

---

## 📊 Analysis (Q1–Q21)

| Q.No | Analysis Question                                       | Insight                                  |
|------|----------------------------------------------------------|------------------------------------------|
| 1    | Total number of records?                                | Retrieved using `df.shape`               |
| 2    | Missing values?                                         | Cleaned & filled                         |
| 3    | Data types?                                             | Verified post-cleaning                   |
| 4    | Date range?                                             | Extracted via `.min()` & `.max()`        |
| 5    | Total Submetering column?                               | Successfully created ✅                   |
| 6    | Summary stats (power metrics)?                          | Computed using `.describe()`             |
| 7    | Mean & Std of Total Submetering?                        | Calculated via `.mean()` & `.std()`      |
| 8    | Voltage distribution?                                   | Histogram + KDE plot                     |
| 9    | Correlation (Global Active Power vs Global Intensity)?  | Strong positive correlation              |
| 10   | Correlation with Voltage?                               | Weak negative correlation                |
| 11   | Min & Max power timestamps?                             | Located using conditional filters        |
| 12   | Hourly trend of power usage?                            | Peak hours identified                    |
| 13   | Day-wise usage trend?                                   | Adjusted for natural weekday order       |
| 14   | Total Submetering hourly trend?                         | Line graph visualized                    |
| 15   | Voltage hourly fluctuation?                             | Plotted using `groupby`                  |
| 16   | Monthly power trend?                                    | Bar chart plotted with month order       |
| 17   | Most consuming Sub-metering?                            | **Sub_metering_3 dominates 💡**           |
| 18   | Total Submetering vs Global Active Power correlation?   | ~0.83 (Strong correlation)               |
| 19   | Unmetered energy usage?                                 | Calculated in kWh                        |
| 20   | Anomalous high/low hours?                               | Identified via ±1 std deviation          |
| 21   | Peak Total_Submetering hour?                            | Extracted & reported                     |

---

## 📈 Visualizations

The following plots were used to illustrate insights:

- Histogram  
- KDE Density Plot  
- Hourly & Daily Line Charts  
- Monthly & Day-wise Bar Charts  
- Scatter Plots with Regression Lines  
- Correlation Heatmaps  

---

## ✅ Key Findings

- **Sub_metering_3** is consistently the highest energy consumer.  
- **Total_Submetering strongly correlates (0.83) with Global Active Power**, validating its role as a reliable measure of total household consumption.  
- Hourly and daily consumption trends highlight **peak demand periods**, offering potential for energy optimization.  
- A fraction of energy remains **unmetered by sub-meters**, suggesting consumption from appliances not tracked individually.  

---

## ⚙️ How to Run the Analysis

1. **Clone the Repository** 
2. **Install Required Libraries**  
3. **Run the Analysis**  
Open the Jupyter Notebook or Python script to execute the workflow:  
4. **Output**  
The cleaned dataset will be saved as `cleaned_dataset.csv`  
Visualizations and statistical findings can be reviewed within the notebook.  

---




