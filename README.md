# Modelling-Cities-Development-with-OSM
This repository illustrate the methods for extracting features from OSM database and how to use them to simulate the cities' development from time to time with OpenStreetMap Data.

# Table of contents
1. [Data Processing](#data_processing)
    1. [Data Extraction](#extract)
    2. [Edit History Classification](#classification)
2. [Exploratory Data Analysis](#EDA)
    1. [Overall Trend](#EDA1)
    2. [Spatial Analysis](#EDA2)
3. [Statistical Modelling](#statmod)
    1. [Cellular Automata Model](#mod1)
    2. [Deep Neural Network](#mod2)


---

## Data Processing <a name="data_processing"></a>
Here are the steps to be followed to do the feature extraction from OpenStreetMap:

### Data Extraction.ipynb <a name="extract"></a>
This workbook retrieve the edit history of POIs from the original document downloaded from OSM. The cleaned data would contain all the edits of POIs lies within the category under study.

### Edit History Classification.ipynb <a name="classification"></a>
This workbook then further group the edit history into three types: 1.Updates; 2.Closure and 3.New. Each of these 3 types of edits represent the different type of evolution undergoes within our city and allows us 3 different angles to analyse the development of our cities from time to time.


## Exploratory Data Analysis <a name="EDA"></a>

### Overall Trend <a name="EDA1"></a>
<img src="Plot/Monthly_New_London-4.png" width="425"/> <img src="Plot/Monthly_Updates_London-3.png" width="425"/> 

The above plot shows the one-year snapshots for the monthly aggregated new business opened in London in both Pre- and Post- Pandemic periods. 
We present the figures of two periods vertically to make the same months aligned, so that the changes of monthly patterns can be compared more easily. 
The total amount of new businesses opened in the Post-Pandemic period is greater than the one-year snapshot before the cut-off date (2020-03-31). 
There is a rebound from June 2020 to September 2020 where the ease of lockdown happened, subsequently, the number drops back as soon as the second wave begin in autumn 2020.
In terms of the trends in these two periods, no big change has been found for new business opening. Thus, we may need to investigate further and at a more granular level in order to see what has been impacted by the COVID-19 crisis.

However, this can only provide the overview of all new businesses opened. As we are looking into the amenity POIs, which covers 10 sub-categories, we may take a closer look into how each sector has been impacted. 

### Spatial Analysis <a name="EDA2"></a>


## Statistical Modelling <a name="statmod"></a>

### Cellular Automata Model <a name="mod1"></a>


### Deep Neural Network <a name="mod2"></a>
