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
