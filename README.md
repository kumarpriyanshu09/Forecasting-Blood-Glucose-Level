# Forecasting-Blood-Glucose-Level

This project explores time series data to forecast future blood glucose levels using a variety of forecasting models. The goal is to provide predictive insights that can aid in diabetes management and improve the lives of those living with diabetes.

## Project Overview

This analysis utilizes a time-series dataset of blood glucose measurements.  The key objectives are to:
-   Identify patterns and trends in glucose fluctuations.
-   Apply time series forecasting techniques (ARIMA and SARIMA).
-   Evaluate and compare the accuracy of different forecasting models.

## Key Findings

*   **Data Patterns:** Analysis of the time series data revealed distinct patterns of glucose fluctuation, especially after aggregating data to hourly and daily levels. These patterns were used to find appropriate models.
*   **Model Selection:**  The SARIMAX (4,0,2) (2,0,1) model was found to be the most effective based on the Ljung-Box test, AIC, and SBC metrics.
*  **Significance of lags:** Significant time lags were found in the ACF and PACF plots at specific time points, especially around level 24, this indicated the presence of seasonality. These time lags were used to test different models.
*  **Model performance:** The forecast graph indicated that the final model was a good fit by showing a clear relationship between the data points, predictive value and the confidence intervals.

## Files

*   `test.csv`: Contains the test data for forecasting.
*   `train.csv`: Contains the training data for building the models.

## Technologies Used

*   SAS Studio (for data analysis and modeling)
*   Time Series Analysis Techniques
*   ARIMA and SARIMA modeling

## Data Insights
  *   Data was aggregated from minute-level data to hourly and then daily levels to identify trends and implement time series analysis.
  *   Hypothesis testing and regression analysis were performed to identify key factors behind blood glucose fluctuations.
  *   Data visualizations were employed to better understand the data patterns and identify key trends.

## How to Use

1.  Download all the files from this repository.
2.  Import the data files ( `train.csv`) into a database or a statistical tool like SAS Studio.
3.  Run the SQL or SAS scripts.
4.  Use the developed model to predict blood glucose levels from the `test.csv` file.

## README Extras

### Project Genesis

This project originated as an academic exploration into the application of time series forecasting to healthcare data.  We were particularly interested in the challenges of managing diabetes and how predictive analytics could provide solutions.

### Motivation

The motivation behind this project stems from a desire to improve the lives of individuals living with diabetes. Traditional blood glucose monitoring is often reactive and provides limited insight into upcoming fluctuations.  We sought to explore how a predictive model could offer more proactive management tools.

### Limitations

*   **Data Scope:** The dataset used in the project is limited in terms of external factors (like exercise, food intake, stress etc), which can affect blood glucose levels.
*   **Model Complexity:** The chosen model represents a trade-off between simplicity and predictive power, it may require further optimization to address complexities of real-world glucose fluctuations.
* **Generalizability**: While this dataset demonstrates our forecasting approach, the model's performance may vary across diverse patient populations and datasets.

### Challenges

*   **Data Preprocessing:**  Aggregating the data into meaningful time intervals required an understanding of time series analysis
*   **Parameter tuning:** Deciding on parameters that can provide the most optimal model for the data was challenging.
*   **Balancing Predictive Power and Generalization:** Striking a balance between model complexity and generalization was a significant hurdle.

### What Problem This Project Solves

This project is a step towards addressing the problem of unpredictable blood glucose fluctuations in individuals with diabetes. By creating a predictive model, it can help:
    *  Individuals better anticipate their glucose levels, aiding in proactive management.
    * Healthcare providers to improve treatment plans by using these predictive insights.

### Intended Use

The intended use of this model is as a proof-of-concept for building an early warning system that alerts users of potential glucose spikes or drops. It is also intended to provide a basis for research in more complex models that might be used in actual wearable tech.
