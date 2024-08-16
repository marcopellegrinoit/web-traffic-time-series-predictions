# Forecast Web Traffic Demand Time Series with ARIMA+ BigQuery and Looker Studio

Author: Marco Pellegrino\
Year: 2024

Forecast Web Traffic Demand using ARIMA+ on GCP BigQuery, and visualize insights in Looker Studio.
Additional data modeling is locally performed with ARIMA, LSTM, and Facebook Prophet.

## Table of Contents

1.  [Description](#description)
2.  [Data](#data)
3.  [Install Required Libraries](#install-required-libraries)
4.  [Project Structure](#project-structure)
5.  [License](#license)

## Description

The project includes both SQL code to be run on BigQuery and Python code to execute the same analysis on a local machine.

*   Data retrieval from Kaggle
*   Data insertion in BigQuery table
*   EDA trends (both in SQL with BigQuery & Looker Studio, and in Python)
*   Stationarity test of a selected page time series (in Python)
*   Forecasting
    *   ARIMA+ (SQL with BigQuery)
    *   ARIMA (Python)
    *   LSTM (Python)
    *   Facebook Prophet (Python)

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

## License

This repository is licensed under the GNU General Public License v3.0 (GPL-3.0). For more details, see the [LICENSE](LICENSE) file.