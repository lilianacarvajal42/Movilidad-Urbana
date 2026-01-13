# Urban Mobility vs. Economic Productivity Analysis

## Project Overview
This project analyzes the relationship between urban mobility (traffic congestion) and economic productivity across major Latin American cities. By integrating real-world traffic data with economic indicators, the analysis identifies cities where transportation inefficiency may be hindering economic growth, providing a data-driven basis for infrastructure investment recommendations.

## Objectives
* **Evaluate** the impact of traffic congestion on city-level GDP and productivity.
* **Clean and Integrate** disparate datasets from TomTom and the OECD.
* **Identify** priority cities (e.g., Bogotá, Lima, Buenos Aires) that show strong correlations between high congestion and low economic performance.

## Datasets
The analysis utilizes two primary data sources:
1.  **TomTom Traffic Index:** Contains metrics on traffic jams, congestion length, and travel delays.
2.  **OECD Cities Economy:** Contains economic data including GDP per capita, unemployment rates, and population statistics.

## Project Structure
The analysis is conducted through the following steps in the Jupyter Notebook:

### 1. Data Loading & Exploration
* Initial inspection of dataset structures, column names, and data types.
* Identification of missing values and inconsistencies.

### 2. Data Cleaning & Preparation
* **Normalization:** Standardizing column names to `snake_case`.
* **Type Conversion:** Formatting dates to `datetime64` and cleaning numerical strings (GDP, unemployment).
* **Feature Engineering:** Calculating population scales and relevant economic ratios.

### 3. Integration & Aggregation
* Aggregating traffic metrics by city and year.
* Performing an `INNER JOIN` to merge traffic data with OECD economic indicators.

### 4. Analysis & Visualization
* Visual validation using distribution plots and trend analysis.
* Outlier detection to identify cities with anomalous traffic-to-productivity ratios.

## Requirements
To run the notebook, ensure you have the following Python libraries installed:
```bash
pip install pandas numpy seaborn matplotlib
```
## 🔍 Preliminary Findings
Based on the integrated analysis of the TomTom and OECD datasets, the following patterns were observed:

* **Congestion vs. Productivity:** Initial trends indicate a measurable correlation between high congestion indices and stagnation in GDP per capita across key Latin American hubs.
* **City Specifics:** Cities like **Bogotá, Lima, and Buenos Aires** were identified as critical points of interest. Bogotá, in particular, shows significant travel delays that align with high economic density, suggesting it is a primary candidate for transit infrastructure investment.
* **Data Anomalies:** Certain outliers were detected where high congestion does not immediately correlate with low productivity, suggesting the presence of robust alternative transport networks or specific urban layouts that mitigate economic loss.



## 🛠 How to Use
To replicate this analysis or apply it to new datasets, follow these steps:

1.  **Environment Setup:** Ensure you have Python installed with the necessary dependencies:
    ```bash
    pip install pandas numpy seaborn matplotlib
    ```
2.  **Data Placement:** Place the raw CSV files for the *TomTom Traffic Index* and *OECD Cities Economy* in the same directory as the notebook.
3.  **Execution:** Open `mobility_economy_project.ipynb` in a Jupyter environment or Google Colab and run the cells sequentially.
4.  **Customization:** You can modify the `city` or `year` filters in the "Filtering & Aggregation" section to focus on different regions or timeframes.

## 💡 Recommendations
* **Priority Investment:** Prioritize infrastructure projects in cities identified in the "High Delay/High GDP Impact" quadrant of the analysis.
* **Source Validation:** It is recommended to cross-reference the 2024 TomTom projections with actual quarterly economic reports to refine the accuracy of the productivity impact.
* **Further Analysis:** Future iterations should include a "Public Transport Accessibility" variable to see if mass transit offsets the economic drag of vehicular traffic.
