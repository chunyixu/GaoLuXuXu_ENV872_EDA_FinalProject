## Summary

<This repository includes the code, datasets (raw and processed), and output used for the project focused on interconnected environmental challenges: CO₂ emissions, renewable energy, and air pollution in the context of UN Sustainability Goals. 

This project explored the correlation between CO₂ emissions and renewable energy use, PM2.5 exposure, and clean cooking access in two developed (USA, Germany) and two developing (China, Colombia) countries from 2010 to 2020. Comparative analysis, correlation analysis, and time-series analysis were leveraged to complete the project. 

We chose this topic because these indicators reflect critical goals under the UN Sustainable Development Agenda—SDG 7 (Clean Energy), SDG 13 (Climate Action), and SDG 3 (Health). Understanding these links helps support more effective, equitable policy solutions.>

## Investigators

<Gao Jie, Master of Environmental Management student at Duke University, j.gao@duke.edu;
Lu Liu, Master of Public Policy student at Duke University, lu.liu@duke.edu；
Chunyi Xu, Master of Public Policy student at Duke University, chunyi.xu@duke.edu;
Ruoran Xu, Master of Environmental Management student at Duke University, rx60@duke.edu>

## Keywords

<Sustainable Development; CO₂ Emissions; Renewable Energy; Air Pollution; UN SDGs>

## Database Information

<The dataset was collected from the World Bank Databank, specifically the World Development Indicators. This is a comprehensive and reliable database compiled from officially recognized international sources. The date of access is April 3, 2025.>


## Folder structure, file formats, and naming conventions 

<This repository contains four folders for raw data, processed data, code, and output respectively. Raw and processed data folders contain Excel data files for data wrangling and storage, while the code and output folders include R scripts.

Files are named according to the following naming convention: 

`Country_Datadescription_Stage.format`, where: 

**Country** refers to the country where the data originated

**Datadescription** is a description of data 

**Stage** refers to the stage in data management pipelines (e.g., raw, cleaned, or processed)

**Format** is a non-proprietary file format (e.g., .csv, .txt)>


## Metadata
<The dataset includes standardized fields for country, year, and key environmental indicators—CO₂ emissions, renewable energy use, and PM2.5 exposure—clearly labeled with appropriate units for cross-country analysis and modeling.> 

**Main Processed Dataset (`Sus_Env_Processed.xlsx`):**

| Column Name    | Description                                      | Data Type | Unit                                  |
|----------------|--------------------------------------------------|-----------|---------------------------------------|
| Country Name   | Full name of the country                         | Character | –                                     |
| Country Code   | ISO 3-letter code                                | Character | –                                     |
| Series Name    | Indicator (CO2, PM, Renew)                       | Character | –                                     |
| Year           | Year of observation                              | Integer   | Year                                  |
| Value          | Measured value of the indicator                  | Numeric   | Varies by Series (see below)          |

**Units by Series:**
- `CO2`: Metric tons per capita
- `Renew`: % of total final energy consumption
- `PM`: µg/m³ (micrograms per cubic meter)

## Scripts and code
All R scripts used for data handling and analysis are stored in the `/code/` directory. These scripts use the following packages:

- `tidyverse`, `readxl`, `writexl` for data import and cleaning
- `ggplot2` for data visualization
- `dplyr` and `lubridate` for data transformation
- `knitr` for formatted output and table rendering

**Script Purposes:**
- Data Wrangling: Cleaning raw WDI Excel files and reshaping to tidy format
- Exploratory Analysis: Generating summary statistics and trends
- Statistical Modeling: Running correlation tests, linear regressions, and AIC model comparisons
- Visualization: Producing line plots, scatterplots, and regression visuals for CO₂, PM2.5, and renewables
