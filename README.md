### Project Report: Analysis and Prediction of Household Power Consumption

#### Overview
This project focuses on analyzing and predicting household electricity consumption using a real-world dataset from the UCI Machine Learning Repository ("Individual Household Electric Power Consumption"). The dataset contains minute-by-minute measurements of power usage, including global active power, voltage, and sub-metering data (kitchen, laundry, and HVAC systems) for a household. The objective was to explore energy consumption patterns, visualize key trends, and build a predictive model using Python.

#### Methodology
1. **Data Preparation:**
   - The dataset (`household_power_consumption.txt`) was loaded using Pandas, with proper handling of missing values (`'?'` replaced with NaN) and conversion of numeric columns to float types.
   - A `DateTime` index was created by combining the `Date` and `Time` columns, parsed in `DD/MM/YYYY HH:MM:SS` format with `dayfirst=True`.

2. **Data Selection:**
   - Data for December 16, 2006, was extracted for analysis. A fallback mechanism ensures the first available day is used if the specified date is missing.

3. **Exploratory Analysis:**
   - Key statistics were calculated for the selected day, including average and maximum global active power, and total energy usage for sub-metering categories.

4. **Visualization:**
   - **Plot 1:** A line chart of global active power over time (hours of the day), highlighting consumption trends.
   - **Plot 2:** A multi-line chart comparing energy usage across sub-metering categories (kitchen, laundry, HVAC).
   - **Plot 3:** A scatter plot with a regression line comparing actual vs. predicted power consumption.

5. **Predictive Modeling:**
   - A linear regression model was trained using time (minutes since midnight) as the feature and global active power as the target.
   - The dataset was split into 80% training and 20% testing sets, and the model’s performance was evaluated using Mean Squared Error (MSE).

#### Results
- **Daily Summary (December 16, 2006):**
  - Average Global Active Power: 3.05 kW
  - Maximum Global Active Power: 7.71 kW
  - Total Sub_metering_1 (Kitchen): 0.00 Wh
  - Total Sub_metering_2 (Laundry): 546.00 Wh
  - Total Sub_metering_3 (HVAC): 4926.00 Wh
- **Visualization Insights:**
  - The global active power plot shows fluctuations throughout the day, with peaks likely corresponding to high-demand periods.
  - Sub-metering analysis reveals that HVAC systems (Sub_metering_3) dominate energy usage, contributing 4926 Wh, while the kitchen (Sub_metering_1) shows negligible consumption (0 Wh), and laundry (Sub_metering_2) accounts for 546 Wh.
- **Prediction Performance:**
  - The linear regression model achieved an MSE of 0.6531, indicating moderate accuracy in predicting power consumption based on time alone. The actual vs. predicted plot shows a reasonable fit, though some variability remains unexplained.

#### Conclusion
This project demonstrates the application of data science techniques to energy management, a field relevant to accounting, economics, and digital skills. The analysis highlights the dominance of HVAC systems in household energy use, offering insights for cost optimization or energy efficiency strategies. The predictive model, while simple, provides a foundation for forecasting power needs, which could be enhanced with additional features (e.g., voltage, sub-metering data) or more advanced algorithms (e.g., Random Forest).

#### Tools and Skills
- **Python Libraries:** Pandas (data manipulation), Matplotlib/Seaborn (visualization), Scikit-learn (machine learning).
- **Skills Demonstrated:** Data cleaning, exploratory data analysis, time-series visualization, and basic predictive modeling.

#### Future Improvements
- Incorporate additional features (e.g., voltage, weather data) to improve prediction accuracy.
- Extend the analysis to multiple days or months for broader trends.
- Experiment with advanced models like ARIMA or neural networks for time-series forecasting.

![download (2)](https://github.com/user-attachments/assets/b70d3c24-45fe-4cc8-aef2-5a67cd3c2f87)
