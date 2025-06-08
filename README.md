# Inflation

# Objective
This project is my attempt to establish a compilation of relevant functions to import, analyse and visualise UK inflation data.

# Progress
So far, I have create the following files:

1. ons.ipynb
    - This is intended to test the ONS's [API](https://developer.ons.gov.uk) with the aim of being able to programmatically obtain UK RPI and CPI index level inflation data
    - Given that I was initially focussing on RPI, i was disappointed to find that the RPI data series does not seem to be available via the API.
    - I will come back to this if/when I am ever looking to pull in CPI data as it does appear to be present (although I have not yet got it working).

2. rpi.ipynb
    - Having ditched the ONS API, i manually downloaded the RPI index .csv file available [here](https://www.ons.gov.uk/economy/inflationandpriceindices/timeseries/chaw/mm23), and dropped it into the `data/` subdirectory
    - This allowed me to create a function to plot the monthly index evolution and the monthly YoY values
    - I then spent some time trying to implement a historical seasonality calculation.
        - Source: [ILB Seasonality Working Paper](https://cnofrance.org/wp-content/uploads/2021/05/2016_06_01-Analyse-Marche-de-Taux-–-Index-linked-bond-Price-Seasonality-.pdf)
    - I believe this is now working the way intended.