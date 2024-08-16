# Forecast Web Traffic Demand Time Series with ARIMA+ BigQuery and Looker Studio

Author: Marco Pellegrino\
Year: 2024

Forecast Web Traffic Demand using ARIMA+ on GCP BigQuery, and visualize insights in Looker Studio.
Additional data modeling is locally performed with ARIMA, LSTM, and Facebook Prophet.

Given historical data, this work can be applied to business case studies where it is required to forecast a generic demand for services or goods.

## Table of Contents

1.  [Description](#description)
2.  [Data](#data)
3.  [Install Required Libraries](#install-required-libraries)
4.  [Project Structure](#project-structure)
5.  [License](#license)

## Description

The project includes both SQL code to be run on BigQuery and Python code to execute the same analysis on a local machine.

*   [Data retrieval from Kaggle](notebooks/1a-retrieve_data_locally.ipynb)
*   [Data insertion in BigQuery table](notebooks/1b-initialize_bigquery.ipynb)
*   EDA trends (both in [SQL with BigQuery & Looker Studio](notebooks/2_EDA_general-BigQuery_Looker.ipynb), and in [Python](notebooks/2_EDA_general-Python.ipynb))
*   [Stationarity test of a selected page time series in Python](2_EDA_individual-Python.ipynb)
*   Forecasting
    *   [ARIMA+ (SQL with BigQuery)](3_ARIMA_PLUS-sql.ipynb)
    *   [ARIMA (Python)](3_ARIMA.ipynb)
    *   [LSTM (Python)](3_LSTM-univariate.ipynb)
    *   [Facebook Prophet (Python)](3_Prophet.ipynb)

## Data

The dataset consists of approximately 145k time series. Each of these time series represents several daily views of a different Wikipedia article, from July 1st, 2015, until December 31st, 2016.

Source: [https://www.kaggle.com/c/web-traffic-time-series-forecasting/data](https://www.kaggle.com/c/web-traffic-time-series-forecasting/data)

## Install Required Libraries

To install the required Python libraries:

```plaintext
pip install -r requirements.txt
```

Note: In some environments, use `pip3` instead of `pip`.

The code has been tested with Python 3.11.

## Sources

*   https://www.clairvoyant.ai/blog/web-traffic-time-series-predictions-using-lstm-and-arima-model
*   https://github.com/jyshao1/web_traffic_time_series/blob/master/web_traffic_time_series.ipynb
*   https://medium.com/datainc/time-series-analysis-and-forecasting-with-arima-in-python-aa22694b3aaa

## Further development
Since the data contains a time series for different pages, each with different characteristics such as language and seasonalities, it would be interesting to implement the new multivariate [ARIMA+ XREG](https://cloud.google.com/bigquery/docs/reference/standard-sql/bigqueryml-syntax-create-multivariate-time-series) model of BigQuery.

## License

This repository is licensed under the GNU General Public License v3.0 (GPL-3.0). For more details, see the [LICENSE](LICENSE) file.