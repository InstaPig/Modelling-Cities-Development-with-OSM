# Modelling-Cities-Development-with-OSM

This repository illustrate the methods for extracting features from OSM database and how to use them to simulate the cities' development from time to time with OpenStreetMap Data. Incorporating the socio-economic variables that describe the cities' profile, we are able to determine the key drivers of cities' developments at different period of time. Further, we can also build models to predict its developments in the futures with the use of predictive modelling.

<p align="center">
  <img width="600"  src="Plot/openstreetmap-2.png">
</p>

A case study of how the cities' developments varied before and after COVID-19 is presented:
- First, we have put the ubiquitous corwd-sourced data into meaningful context. In particular, we have shown how to retrieve historical data from OpenStreetMap and proposed a evaluation metric to quantify the undergoing changes within cities. 
- With various source of information incorporated, we then examined the relationship between these changes and the different type of indicators, including geodemographic factors, temporal variable and the surrounding effect. 
- Subsequently, we compared such relationships before and after the outbreak of COVID-19 pandemic and evaluate the difference between the two periods of time, as well as determine the changes across different cities.
- Finally, we extend our idea to real-life application based on the quantified undergoing changes of the city, to predict which area are likely to engage a huge development in the future by using both Cellular Automata model and deep neural network.

<p align="center">
  <img height="300"  src="Plot/Social Economic Factors.png"> <img height="300"  src="Plot/UK_Map.png">
</p>


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
This workbook retrieve the edit history of POIs from the original document downloaded from OSM. The cleaned data would contain all the edits of POIs lies within the category under study. An example of extracted data can be find below:

<p align="center">
  <img width="600"  src="Plot/Tabular Data Example.png">
</p>

### Edit History Classification.ipynb <a name="classification"></a>
This workbook then further group the edit history into three types: 1.Updates; 2.Closure and 3.New Opening. Each of these 3 types of edits represent the different type of evolution undergoes within our city and allows us 3 different angles to analyse the development of our cities from time to time.

With the above defined measures, we can count the number of edits for all types within each part of city (e.g. at the level of Ward). This aggragated amount gives us an idea how active the evolution is going on in each part of the city. Further, with the use of other socio-economic factors, we will then be able to model its relationship with the cities' profile. So that, we will be able to determine the key drivers behind the cities' development during each period.

## Exploratory Data Analysis <a name="EDA"></a>

### Overall Trend <a name="EDA1"></a>
<p align="center">
<img src="Plot/Monthly_New_London-4.png" width="350"/> <img src="Plot/Monthly_Updates_London-3.png" width="350"/> 
</p>
The above plot shows the one-year snapshots for the monthly aggregated new business opened in London in both Pre- and Post- Pandemic periods.  

- The total amount of new businesses opened in the Post-Pandemic period is greater than the one-year snapshot before the cut-off date (2020-03-31). 
- There is a rebound from June 2020 to September 2020 where the ease of lockdown happened, subsequently, the number drops back as soon as the second wave begin in autumn 2020.

In terms of the trends in these two periods, no big change has been found for new business opening. Thus, we may need to investigate further and at a more granular level in order to see what has been impacted by the COVID-19 crisis.As we are looking into the amenity POIs, which covers 10 sub-categories, we may take a closer look into how each sector has been impacted. 

### Spatial Analysis <a name="EDA2"></a>
<p align="center">
<img src="Plot/New_Choropleth_Map-3.png" width="350"/> <img src="Plot/Update_Choropleth_Map-3.png" width="350"/> 
</p>

**Pattern of New Business Openings:**

The above plots shows the pattern of new businesses opened during the one-year interval before and after the outbreak of COVID:

- The new business opened in the one year interval before the outbreak of pandemic mainly concentrated around the built-up areas of Greater London and has only very few spread across the suburbs. 
- New businesses established during the one-year period after the outbreak of pandemic spread more widely across the entire area under study with a quite significant portion in those suburban areas. 

To some extend, this change reflects the increasing demands in various types of facilities and services in the suburbs where some of them were not established locally in the past. 
As before lockdown, commuting is much more convenient and people live in suburbs can access those services that are perhaps only available in the built-up areas easily. 
But now, the restrictions and social scarring have changed this, and thus brought opportunities for these services to be established locally. This also explains why we have seen a increase in the average number of new business (among all amenity types) during the post-pandemic period shown in the plot.

**Pattern of Amendments Made on Businesses:**

Now, looking into the variation in measurements of updates shown by the plots, it grants us another angle to analyse the impacts of COVID on cities' evolution. 
- Although the updates have taken place in almost everywhere in London during the one-year timeframe before the crisis started, a very obvious tendency of spreading into non-built-up areas can still be seen in the one-year time after the cut-off point. 
- In fact, not only the coverage has expanded, but also the number of updates increased in the suburbs.There is not doubt that businesses need to have more amendments in response to the restrictions and virus. So, we see more obvious increases of such measurement in the ares surrounding the centre.

For the build-up areas at the centre, the amount of updates stay approximately the same in the two periods. There are two potential reasons why they have the highest amount of updates: 
- They have a larger base (more businesses in operation) compared to other areas. 
- In the past, businesses within these areas may need frequent adjustments potentially due to their commercial strategy or other events that only held in the city centre such as marathon.

However, these events were mostly canceled due to the epidemic, thus the areas has the most concentrated adjustments owing to their large foundations of business and the needs of amendments due to restrictions that applied to all wards.

## Statistical Modelling <a name="statmod"></a>

### Cellular Automata Model <a name="mod1"></a>


### Deep Neural Network <a name="mod2"></a>
