# Analyzing the Impact of Smoke on Agricultutal Productivity 

## Overview
This project explores the intersection of wildfire smoke, air quality, and agricultural productivity in Omaha, Nebraska, with a focus on corn and soybean crops. The study includes constructing a smoke estimate from fire data, analyzing crop yield and condition trends, and employing advanced time-series forecasting techniques to predict future risks. 

The analysis aims to provide actionable insights for policymakers, farmers, and researchers to better understand the implications of wildfire smoke and take proactive measures for resilience.

## Data Sources
### Primary Sources
1. **Fire Data**:  
   - Acquired from [U.S. Geological Survey (USGS)](https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81).  
   - Contains historical fire event information, including burnt area and geospatial details.

2. **Agricultural Data**:  
   - **Corn and Soybean Yields**: [USDA National Agricultural Statistics Service (NASS) Quick Stats](https://quickstats.nass.usda.gov/results/DE7B9199-B43E-32AB-B0E7-677D7F05CAE1).  
   - **Crop Conditions**: [USDA NASS Quick Stats](https://quickstats.nass.usda.gov/results/DD0A20B2-18BB-3945-97B2-9B4A5FAC1DED).

3. **Air Quality Index (AQI) Data**:
   - Obtained via the [US Environmental Protection Agency (EPA) Air Quality System (AQS) API](https://aqs.epa.gov/aqsweb/documents/data_api.html#daily). The data contains daily summaries of gas and particulate air quality measurements.

### Supplementary Sources
- **Wildfire Effects on Crops**: Reports from [Bayer Crop Science](https://www.cropscience.bayer.us/articles/bayer/wildfire-smoke-on-crops) and [Pioneer Agronomy](https://www.pioneer.com/us/agronomy/wildfires-crop-yields.html#PotentialEffectsOfSmokeOnCrops_3).

## Modelling Techniques
The study employs advanced time-series forecasting models to analyze historical data and project future trends:
1. **Meta's Prophet**:  
   - Open-source forecasting model designed for interpretable analysis of seasonal and trend components.  
   - [Learn more](https://facebook.github.io/prophet/).
   
2. **Exponential Smoothing**:  
   - A statistical technique that assigns exponentially decreasing weights to older observations for time series forecasting.

3. **Ordinal Logistic Regression**:  
   - Used to explore the relationship between smoke estimates and crop condition categories.

4. **Vector Autoregression (VAR)**:  
   - Explored for dynamic interdependencies between smoke, yields, and other variables.

## Key Findings
1. **Smoke Estimates**: Developed a model using fire data with assumptions of radial and uniform smoke dispersion.  
2. **Crop Trends**:  
   - Corn and soybean yields show a steady upward trend due to technological advancements.  
   - Smoke estimates exhibit moderate correlation with crop yields, but no causal relationship was established.  
3. **Crop Conditions**: No statistically significant evidence was found linking smoke estimates to variations in crop conditions.

## Intermediate Files
### Generated Data Files
## Intermediate Files

The aqi_data_acquisition.ipynb notebook is responsible for generating the intermediate files containing the AQI data.

1. **particulate_aqi.json**
   - **Description**: Contains daily summaries of particulate AQI for Omaha, NE from 1970 onwards.

2. **gaseous_aqi.json**
   - **Description**: Contains daily summaries of gaseous AQI for Omaha, NE from 1970 onwards.
  
The smoke_estimate_creation.ipynb notebook is resposnible for generating the following intermediate files.
1. **forecasted-smoke_estimates.csv**:  
   - Forecasted smoke estimates derived from fire data for Omaha, NE using Meta's Prophet model.  

2. **smoke_estimates.csv**:  
   - Contains smoke estimates calculated for years 1960-2020 using the formula smoke estimate = burnt area / (distance of fire centroid from city center)^2

## Code and Documentation
All analysis, data cleaning, and modelling processes are documented in the main [Jupyter notebook](https://github.com/manya28/data-512-project/blob/main/main.ipynb). Key steps include:  
- Data acquisition and preprocessing  
- Smoke estimate construction

All analysis, data cleaning and modelling for establishing relationship of smoke estimate with agricultutral productivity are documented in the main-project . Key steps include:
- Exploratory data analysis (EDA)  
- Time series and regression modelling  

## License
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

### Data and Model Licensing
- **Fire Data**: U.S. Geological Survey (USGS) - Public Domain.  
- **Agricultural Data**: USDA NASS - Public Domain.  
- **Meta's Prophet**: MIT License.

## Reflection
A detailed reflection on the project methodology and insights can be found [here]([Final Project Report - DATA 512.pdf](https://github.com/manya28/data-512-project/blob/main/Final%20Project%20Report%20-%20DATA%20512.pdf)).

## Acknowledgements
- **Meta's Prophet** for time-series modelling.  
- **USGS** for providing comprehensive fire data.  
- **USDA NASS** for agricultural yield and condition data.  
- **CropWatch** and **ClimateCheck** for climate and drought insights.  
- **ChatGPT by OpenAI** for assistance in documentation and refining the analysis.
