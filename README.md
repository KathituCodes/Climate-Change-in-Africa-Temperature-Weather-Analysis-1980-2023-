# 🌍 Climate Change in Africa: Temperature & Weather Analysis (1980–2023)

This project explores temperature and weather patterns across five African countries — Senegal, Egypt, Cameroon, Tunisia, and Angola — using a historical dataset covering 1980–2023 provided by the [U.S. Global Change Research Program](https://www.globalchange.gov/). The goal is to gain insights into how climate features have evolved and relate to each other in these regions over the past four decades.

🎯 **Objective**
The main objective of this project is to analyze the 'Climate Change in Africa' dataset by visualizing temperature fluctuations and other weather patterns across the selected countries from 1980 to 2023.

📁 **Dataset Description**
The dataset contains daily records of:

* Minimum temperature (`TMIN`)
* Maximum temperature (`TMAX`)
* Average temperature (`TAVG`)
* Precipitation (`PRCP`)

* **📆 Time Period:** 1980 – 2023
* **📍 Countries:** Egypt, Tunisia, Cameroon, Senegal, Angola
* **📤 Source:** Derived from NOAA Global Surface Summary of the Day (GSOD) data (Implicitly, often used in such analyses - confirm if source is explicitly known)
* ➡️ **Dataset:** `africa climate change.csv` (as loaded in the notebook)

🧪 **Tasks Performed**

1.  **Data Loading and Cleaning:**
    * Imported the dataset using pandas.
    * Converted the `DATE` column to datetime objects.
    * Extracted `Year` and `Month` for temporal analysis.
    * Handled missing values using the `MEAN` since we dealing with continuous numerical data.
    * Filtered the dataset to include only the five target countries.

2.  **Temperature Trend Analysis (Tunisia & Cameroon):**
    * Plotted a line chart showing the yearly average temperature (`TAVG`) fluctuations in Tunisia and Cameroon from 1980 to 2023.
    * *Visualization Title:* "Average Temperature Trend in Tunisia and Cameroon (1980-2023)"
    * *Key Insight:* Observed general warming trends in both countries over the period.

3.  **Temperature Distribution Analysis (Senegal):**
    * Created overlapping histograms to compare the distribution of average daily temperatures (`TAVG`) in Senegal between two periods:
        * 1980–2000
        * 2001–2023
    * *Visualization Title:* "Distribution of Average Temperatures in Senegal (1980-2000 vs 2001-2023)"
    * *Key Insight:* The distribution suggests a shift towards higher average temperatures in the more recent period (2001–2023).

4.  **Comparing Average Temperatures Across Countries:**
    * Calculated the overall average temperature (`TAVG`) for each country across the entire time span (1980-2023).
    * Selected and created a bar chart to clearly display and compare these country-level averages.
    * *Visualization Title:* "Average Temperature by Country (1980-2023)"

5.  **Exploratory Data Analysis & Questions:**
    * **Q1: Which country experienced the highest recorded max temperature?**
        * Identified the maximum `TMAX` value in the dataset and the corresponding country/date.
    * **Q2: Are there seasonal patterns across countries?**
        * Calculated monthly average temperatures (`TAVG`) for each country.
        * Visualized seasonal patterns using:
            * Line plots showing monthly averages per country. (*Viz Title: "Average Monthly Temperature Patterns by Country"*)
            * A heatmap comparing monthly average temperatures across countries. (*Viz Title: "Heatmap of Average Monthly Temperatures by Country"*)
            * Boxplots showing the distribution of average temperatures (`TAVG`) for each country. (*Viz Title: "Distribution of Average Temperatures by Country"*)
    * **Correlation Analysis:**
        * Calculated the correlation matrix between `PRCP`, `TAVG`, `TMAX`, and `TMIN`.
        * Visualized the correlations using a heatmap.
        * *Visualization Title:* "Correlation Between Weather Features"
        * *Key Insight:* Temperature variables (`TAVG`, `TMAX`, `TMIN`) are strongly positively correlated, while precipitation (`PRCP`) shows very weak correlation with temperatures in this dataset.

📊 **Visualizations Preview**

<details>
<summary>Click to expand</summary>

* Line chart: "Average Temperature Trend in Tunisia and Cameroon (1980-2023)"
* Overlapping Histograms: "Distribution of Average Temperatures in Senegal (1980-2000 vs 2001-2023)"
* Bar chart: "Average Temperature by Country (1980-2023)"
* Line chart: "Average Monthly Temperature Patterns by Country"
* Heatmap: "Heatmap of Average Monthly Temperatures by Country"
* Boxplots: "Distribution of Average Temperatures by Country"
* Heatmap: "Correlation Between Weather Features"

</details>

🛠️ **Tools & Libraries**
* Python
* pandas
* numpy
* matplotlib
* seaborn

🤔 **Conclusion**
The analysis highlights noticeable temperature trends and patterns across the selected African nations. Warming trends are suggested by the time-series plots and comparative histograms. Seasonal patterns are evident, and while temperature metrics are closely related, precipitation appears largely independent of temperature in this dataset. This exploration provides a valuable lens into regional climate characteristics and changes over the analyzed period.

📌 **To-Do / Future Work**
* Incorporate additional climate variables (e.g., humidity, wind speed) if available.
* Extend analysis to other African nations or regions.
* Apply time series decomposition or modeling techniques for deeper trend/seasonality analysis.
* Build a web-based dashboard for interactive visualization.
