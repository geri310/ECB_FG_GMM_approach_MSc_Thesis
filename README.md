# ECB monetary policy effect on private sector expectations
## roadmap of this repository
There are to branches: master (last thesis code) and archive (where all the old code is pushed).
### master branch

**What is in the data folder**: Contains all the data needed for the thesis - both the raw data and the already processed data.

1. **Raw data files**:
    - Dataset_EA-MPD.xlsx: the [EA-MPD](https://www.ecb.europa.eu/pub/pdf/scpwps/ecb.wp2281~3303fd281b.en.pdf) dataset, containing OLS changes 
    - SPF_rounds_dates.xlsx: the dates for [ECB private sector forecasts](https://www.ecb.europa.eu/stats/ecb_surveys/survey_of_professional_forecasters/html/index.en.html)
    - ecb_proj.xlsx: already downloaded ECB projections
    - 1991Q1.csv ... 2020Q1.csv: data from the [ECB survey of professional forecasters](https://www.ecb.europa.eu/stats/ecb_surveys/survey_of_professional_forecasters/html/index.en.html)
2. **Processed dataframes**:
    - infl_data.pkl, un_data.pkl, gdp_data.pkl: product of the orderly data notebook. These are the complied dataframes with all the forecasts.
    - ecb* files: product of the ECB projections notebook. currently not used.
    - GMMsGDP.pkl: the estimates of the individual per source GMMs estimates for GDP changes in forecast.
    
**All the code**:
- thesis_orderlydata.ipynb: reads the raw data for the ECB survey of professionals forecasts and generates the combiled, easy-to-use dataframes.
- gmmINFL/GDP/UNR-Averages.ipynb: three notebooks (INFL/GDP/UNR), for the GMM estimates of the average of the forecasts for inflation, GDP, and unemployment rate. This also includes the cumulative IRs.
- gmmGDP-allsources.ipynb: generates the individual GMMs for GDP (one per source). alternatively, as this takes a while, it loads the data that is already in the Data folder, and plots the confidence intervals.
- ecb-proj.ipynb: descriptive statistics for the ECB projections data, and generates some dataframes (not used currently).
