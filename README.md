# Evaluating Labor Market Dynamics During the 2020 Economic Freeze

A data-driven study exploring the socioeconomic impact of the 2020 COVID-19 lockdowns on the Indian labor market. This project cleans, visualizes, and breaks down key employment parameters across different states, geographic zones, and sectors (urban vs. rural).

---

## 📌 Project Overview
The strict 2020 pandemic lockdowns created unprecedented changes in global labor forces. This project aims to mathematically isolate the lockdown shock from regular seasonal trends in India, identify which areas took the hardest hit, and analyze how workforce engagement reacted to an artificial economic freeze.

---

## 🛠️ Data Cleaning & Setup Workflow
Before analyzing the metrics, the raw data was processed using the following pipeline to ensure statistical accuracy:
1. **Header Stripping:** Removed hidden spaces from all column names to prevent reference errors.
2. **Column Standardization:** Cleaned duplicate naming conventions by safely mapping variations like `Region.1` or `Region_macro` into a clean, unified `Macro_Region` feature.
3. **Missing Value Treatment:** Scanned and removed empty records lagging core targets (`Region`, `Date`, or `Unemployment Rate`) to avoid structural biases in charts.
4. **Data Normalization:** Cleaned spaces within row elements (e.g., converting `" Punjab "` to `"Punjab"`) and converted the date text into explicit Python datetime formats (`%d-%m-%Y`) for linear timeline tracking.

---

## 📊 Key Baseline Statistics

Running a descriptive summary analysis across the cleaned database yields the following structural parameters:

* **Estimated Unemployment Rate (%):** Spans a low minimum baseline of **0.50%** up to a catastrophic, historic crisis peak maximum of **75.85%**. While the median (**50% Mark**) sits at **9.65%**, extreme lockdown shocks pull the overall national average up to **12.24%**.
* **Estimated Employed (Total Workforce):** Ranges from **117,542** to **59,433,759** citizens, tracking an operational average of **13.96 Million** workers. This distribution directly mirrors the population footprints of small territories versus massive states.
* **Labour Force Participation Rate (LFPR %):** Displays tight workforce stability with a mean of **41.68%** and a median of **40.39%**. Despite crashing to an absolute minimum of **16.77%** during strict lockdown weeks, upper percentiles show regular bounds returning to **44.06%**.

---

## 📈 Visualizations & Analytical Insights

This repository contains the following key visualizations that track the progression of the 2020 economic shock:

### 1. Overall Data Distribution
* **Filename:** `unemployment_national_average_skew.png`
* **Insight:** Plots how often different unemployment levels occur. It features a right-skewed layout with a vertical line highlighting the **12.24%** national average, showing how the massive 2020 spikes pulled the economy out of its normal **9.65%** center.

### 2. State-Level Performance Ranking
* **Filename:** `sorted_regional_unemployment_comparison.png`
* **Insight:** Groups and ranks average unemployment from highest to lowest by region. It provides an immediate look at which local governments faced the deepest local labor challenges.

### 3. Geographic Volatility & Outliers
* **Filename:** `unemployment_distribution_by_geographic_zones.png`
* **Insight:** A boxplot tracking data dispersion across major macro zones. It highlights that while North India faced high baseline levels, South and East India suffered the most extreme, single-point outlier spikes (exceeding **75%**) during the lockdown window.

### 4. National Labor Timeline Divergence
* **Filename:** `lockdown_labor_market_divergence.png`
* **Insight:** Traces a dual-line timeline mapping Unemployment against Labor Force Participation (LFPR). By shading the strict lockdown window, it shows a visible cross-over effect: as unemployment skyrocketed to **22.75%**, participation collapsed, showing that millions of workers temporarily gave up looking for work entirely.

### 5. Sector Disruption Split
* **Filename:** `urban_vs_rural_unemployment_trend.png`
* **Insight:** Complements the timeline by splitting data into city and village areas. It proves that cities took a harsher hit (peaking near **28%**) because urban businesses were frozen, whereas rural villages were insulated by farming being classified as an "essential service."

### 6. Variable Relationship Interdependency
* **Filename:** `employment_feature_heatmap.png`
* **Insight:** A heatmap visualizing correlation coefficients. It flags a clear negative relationship (**-0.25**) between unemployment and labor participation, confirming the statistical footprint of the "Discouraged Worker Effect."

### 7. Time Series Component Decomposition
* **Filename:** `unemployment_trend_seasonal_residual_plot.png`
* **Insight:** Uses a 3-month cycle model to separate the timeline into Long-Term Trend, Seasonal Shifts, and Random Shocks (Residuals). The flat trend line followed by a vertical jump, paired with isolated, massive residual spikes on the far right, proves mathematically that the pandemic was an artificial shock rather than a normal, cyclical market downturn.

---
