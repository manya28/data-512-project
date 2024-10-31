# Fire and AQI Analysis Project

## Overview
The analysis includes calculating smoke estimates from fire data and estimating AQI levels. The study employs different time series models, such as Meta's Prophet and Exponential smoothing, to explore trends and project future estimates.

## Data Sources
- **Fire Data**: Acquired from [U.S. Geological Survey (USGS)](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81). This dataset contains historical fire event information, including burnt areas and geospatial information.
- **Air Quality Index (AQI) Data**: Obtained via the [US Environmental Protection Agency (EPA) Air Quality System (AQS) API](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily). The data contains daily summaries of gas and particulate air quality measurements.

## Modelling Attribution
The time series modelling was performed using **Meta's Prophet**, an open-source forecasting tool. More information about Prophet can be found here: [Meta's Prophet](https://facebook.github.io/prophet/).

## Intermediate Files
The aqi_data_acquisition.ipynb notebook is responsible for generating the intermediate files containing the AQI data.

1. **particulate_aqi.json**
   - **Description**: Contains daily summaries of particulate AQI for Omaha, NE from 1970 onwards.

2. **gaseous_aqi.json**
   - **Description**: Contains daily summaries of gaseous AQI for Omaha, NE from 1970 onwards.

## Code and Notebook
All of the analysis, data cleaning, and modelling work is documented in the [Jupyter notebook](https://github.com/manya28/data-512-project/blob/main/main.ipynb). This notebook contains the detailed implementation steps, including data acquisition, preprocessing, visualizations, and time series modelling.

## License
This project is licensed under the MIT License.

### Data and Model Licensing
- **Fire Data**: U.S. Geological Survey (USGS) - Public Domain.
- **Air Quality Index (AQI) Data**: US Environmental Protection Agency (EPA) - Public Domain.
- **Meta's Prophet**: Open-source under the [MIT License](https://github.com/facebook/prophet/blob/main/LICENSE).

## Reflection

Find the reflections from this project on https://docs.google.com/document/d/1SKiRPM7VabPD7-67cd1LAmwMG2iwIggVCcUVcv4weTU/edit?usp=sharing 

## Acknowledgements
- **Meta's Prophet** for time series modelling.
- **USGS** for fire data.
- **US EPA** for air quality data through the AQS API.
- **ChatGPT by OpenAI** for assisting in troubleshooting bugs and refining documentation throughout the analysis.

