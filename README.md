#  Electric Vehicle Charging Analysis

This project explores patterns in electric vehicle (EV) charging behavior to uncover insights that can inform infrastructure development, pricing strategies, and user experience improvements. With a dataset of 1,320 EV charging sessions across multiple U.S. cities, we analyze usage across vehicle types, charger categories, time of day, and user segments.

---

##  Table of Contents

- [ Executive Summary](#-executive-summary)
- [ Problem Statement](#-problem-statement)
- [ Dataset Overview](#-dataset-overview)
- [ Data Preprocessing](#-data-preprocessing)
- [ Exploratory Data Analysis](#-exploratory-data-analysis)
- [ Statistical Testing](#-statistical-testing)
- [ Key Insights](#-key-insights)
- [ Recommendations](#-recommendations)
- [ Technologies Used](#-technologies-used)
- [ Project Structure](#-project-structure)
- [ Future Work](#-future-work)

---

## Executive Summary

This analysis investigates EV charging behavior by user type, charger type, time, and location. Key findings include:

- **DC Fast Chargers** deliver faster charging at higher costs.
- **Commuters vs Long-Distance Travelers** show distinct usage patterns.
- **Weekends** show longer, higher-energy charging sessions.
- **Peak charging hours**: 7–9 AM and 5–8 PM.

These findings can help optimize EV charging infrastructure and improve customer satisfaction.

---

##  Problem Statement

With EV adoption rising, charging networks face challenges in:

- **Infrastructure Planning**: Where and what type of chargers are needed?
- **User Segmentation**: How do behaviors vary across user types?
- **Economic Optimization**: How do cost and energy use vary by location/model?
- **Demand Management**: When are peak times, and how can we manage them?

---

##  Dataset Overview

- **Source**: Simulated dataset with 1,320 records.
- **Features include**:
  - `Vehicle Model`, `Battery Capacity`, `User Type`
  - `Charging Start/End Time`, `Energy Consumed`, `Charging Rate`
  - `Charger Type`, `Charging Station Location`
  - `Charging Cost`, `Temperature`, `State of Charge`, etc.

---

##  Data Preprocessing

- **Missing Values**:
  - Imputed with median values grouped by charger type and vehicle model.
- **Outlier Treatment**:
  - Capped `State of Charge`, `Energy Consumed`, `Temperature`.
- **Feature Engineering**:
  - Extracted `Start Hour` from datetime.
  - Created derived metrics for charging patterns.

---

##  Exploratory Data Analysis

### Univariate Analysis

- Distribution of `Energy Consumed`, `Charging Cost`, and `User Type`.

### Bivariate Analysis

- Boxplots: `Energy Consumed` vs `User Type`
- Histograms: `Energy Usage` by `Day of Week` and `User Type`
- Scatter Plots: `Charging Duration` vs `Energy Consumed`

### Time-Based Patterns

- Peak hours: 7–9 AM and 5–8 PM.
- Longer durations and higher energy usage on weekends.

### Categorical Analysis

- `Charger Type` vs `Energy Consumed`
- `Vehicle Model` vs `Charging Cost`
- Location-based usage distribution

### Correlation Heatmap

- Insights into numeric relationships between energy, cost, distance, etc.

---

##  Statistical Testing

- **ANOVA Tests**:
  -  Energy use differs significantly by **Charger Type**
  -  Charging cost varies significantly across **Vehicle Models**
  -  No significant difference in energy consumption by **User Type**

---

##  Key Insights

- **DC Fast Chargers** offer speed but at a premium.
- **Level 2 Chargers** are optimal for balance of speed and cost.
- **Commuters** charge more frequently but use less energy.
- **Long-distance travelers** consume more energy per session.
- Charging activity peaks **morning and evening**.
- **Older vehicles** tend to charge slower and cost more.
- **Temperature** slightly impacts energy use in extreme cold.

---

##  Recommendations

- Expand **DC Fast Chargers** on highways, **Level 2** in urban zones.
- Implement **dynamic pricing** to reduce congestion at peak hours.
- Offer **subscription plans** for frequent users.
- Provide **personalized insights** based on vehicle and usage.
- Partner with automakers (e.g., Tesla) for integration and marketing.
- Enhance apps to show energy saved and charging suggestions.

---

##  Technologies Used

- **Python** (Pandas, NumPy, Seaborn, Matplotlib)
- **Jupyter Notebook / Google Colab**
- **Statistical Testing**: SciPy (ANOVA)
- **Visualization**: Seaborn, Matplotlib

---


