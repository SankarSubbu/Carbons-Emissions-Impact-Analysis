# Carbon Emissions Impact Analysis

## Project Summary

This project analyzes historical atmospheric carbon dioxide (CO2) concentration data to visualize and understand its trend over time. The analysis of the provided dataset reveals a consistent and accelerating increase in global CO2 levels from 1958 to the present day, highlighting the long-term impact of carbon emissions on the atmosphere.

## The Dataset

The core data for this analysis is contained in `carbon_emmission.csv`.

- **Source**: The data is a time series that closely resembles the iconic Keeling Curve from the Mauna Loa Observatory, which is a key benchmark for tracking global atmospheric CO2 concentration.
- **Time Range**: The data spans from March 1958 to early 2024.
- **Columns**:

  - `ObjectId`: A unique identifier for each row.
  - `Country`: The geographical scope of the data. In this dataset, it is consistently 'World'.
  - `Date`: The year and month of the measurement, formatted as `YYYYMmm`.
  - `Value`: The measured value.

- **Data Structure**: The dataset appears to contain two types of `Value` entries for many months. The primary value is a larger number (e.g., `315.7`) representing the average CO2 concentration in parts per million (ppm). A secondary, smaller value (e.g., `0.3`) is also present for some dates, which could represent the measurement uncertainty or the rate of change. This analysis focuses on the primary ppm values to show the overall trend.

## Analysis and Visualization

The primary analysis involves plotting the CO2 concentration (in ppm) against time. The resulting visualization clearly shows two distinct patterns:

1.  **A Seasonal Cycle**: A regular, sawtooth pattern within each year. This is caused by the seasonal cycle of plant photosynthesis in the Northern Hemisphere, which absorbs more CO2 during its growing season.
2.  **A Long-Term Upward Trend**: A steady and steepening upward curve, indicating a continuous and accelerating increase in atmospheric CO2 since the measurements began.

The chart below is a representation of the trend found in the dataset.
! [image alt]https://github.com/SankarSubbu/Carbons-Emissions-Impact-Analysis/blob/e5616268c7e751b6405d6c71f721c76f79de159d/outputs/Seasonal%20Variations%20in%20CO%E2%82%82%20Concentrations.jpeg
## Key Findings

- **Unprecedented Growth**: Atmospheric CO2 levels have risen dramatically, from approximately 315 ppm in 1958 to over 420 ppm in recent years.
- **Accelerating Rate**: The rate of CO2 increase has accelerated over the decades, with recent years showing some of the fastest growth on record.
- **Clear Seasonal Fluctuation**: There is a consistent intra-year fluctuation of about 5-7 ppm, typically peaking in May and reaching a minimum around October.

## How to Use This Project

1.  **Prerequisites**:
    - A data analysis environment like Python with `pandas` and `matplotlib`/`seaborn`, or any other data visualization tool.
2.  **Analysis**:
    - Load the `carbon_emmission.csv` file.
    - Parse the `Date` column into a datetime format.
    - Filter the data to use the primary ppm values for plotting.
    - Create a line chart of `Date` vs. `Value` to replicate the analysis.

## Future Work

- **Forecasting**: Use time series models like ARIMA or Prophet to forecast future CO2 concentrations based on historical trends.
- **Correlation Analysis**: Correlate the CO2 data with other global datasets, such as global temperature anomalies, industrial output, or population growth, to explore relationships.
- **Data Cleaning**: Investigate the secondary `Value` entries to confirm their meaning and potentially incorporate them into a more detailed analysis of measurement uncertainty or monthly change rates.
