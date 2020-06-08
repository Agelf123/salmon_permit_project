Predicting the Value of Bristol Bay Alaska Salmon Drift Permits: Will the Alaskan Salmon Boom Continue?

By: Aryeh Gelfand(https://github.com/Agelf123)


The Problem:

Gelfand Investment wants to invest in the Alaska Salmon Industry . We are looking to buy assets that have risen in value due to the recent strength of the Alaskan Salmon industry.
We have identified Bristol Bay Drift Permits as an asset whose value mirrors the strength of the industry and we believe that the value will continue to rise over the next five years. We also want to know what industry factors contribute to the rise of this asset. 
In order to know if this is a good purchase we will model the value of this asset over the next five years. We will  use RMSE to evaluate if our model is accurate. We want to know to what certainty we can know whether these permits will hold or rise in value over the next five years.


Executive Summary

We wanted to create a forecast for the years 2020-2025 for Bristol Bay Drift Permits. We are focusing on these permits because they do a good job of reflecting the industry and tend to surge in value when the industry is producing profits. We want to know whether or not the current salmon boom will continue. In order to understand the issue, we gathered a massive dataset of potential factors that would help us predict  the fluctuation in this asset. We quickly discovered that the major factors in evaluating this asset were close to home. The top correlative factors for predicting the value of this asset are:

- Southeast Pink Ex Vessel Value
- Bristol Bay Sockeye Nominal Value
- Chignik Pink Ex Vessel Value

This makes a lot of sense, fisheries that are directly related to Bristol Bay Salmon or follow the same trends are extremely helpful in predicting the fluctuations in value of permits. Other factors that were important were seafood consumption in competitive markets like Japan. 

In the end we we able to create a very accurate model within our sample time period and then create a reasonably reliable forecast for the next five years. The other factors were not as helpful in this and we used only the data from permit pricing from the years on record. 

Conclusions and Recommendations

Although the models we ran had a wide confidence interval, given the strength of the industry as a whole and resiliency we have seen, we are comfortable going ahead with the purchase. The Arimax model handled the exogenous variables the best, but in the end the SARIMA outperformed it. Too many features added noise to the model and ended up skewing the results, but we did get a good sense of the features that were correlative in making our prediction.
Moving forward, I would remove some of the fish production and consumption data and only focus on features that really add variance.

Data Dictionary

|Name of Field|Where Table exists|Description|Source|Datatype|
|---|---|---|---|---|
|Fishcount|df_clean|Fish Counts by river for every river system in Alaska| http://www.adfg.alaska.gov/sf/FishCounts/ |float64|
|Ex Vessel Pricing Salmon|df_clean|dock price or price paid to fisherman for salmon by year|https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_exvessel|float64|
|Salmon price by Area|df_clean|Salmon price per pound by area|https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmon_grossearnings_byarea|float64|
|Wholesale value of Salmon|df_clean|'Unique code for each reddit post|https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_wholesale|int64|
|Farm Salmon Pricing|df_clean|price for norwegian farm salmon retail price|https://www.indexmundi.com/commodities/?commodity=salmon&months=360|float64|
|Shrimp |df_clean|price for shrimp on world markets|https://www.indexmundi.com/commodities/?commodity=shrimp&months=360|float64|
|Gross Earnings By Area|df_clean|The gross earnings for each salmon area |https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmon_grossearnings_byarea|float64|
|Gross Earnings By Species|df_clean|gros Earnings for Each salmon Species|https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_wholesale|float64|
|Seafood production and Consumption|df_clean|Seafood Consumption and Production|https://ourworldindata.org/seafood-production|float64|
|Capture Fishing vs Aquaculture|df_clean|capture fishing vs aquaculture|https://ourworldindata.org/seafood-production|float64|
|Bristol Bay Permit Pricing|df_clean|The price of a drift permit for bristol bay salmon|https://www.cfec.state.ak.us/pmtvalue/X_S03T.HTM|float64|


References

https://www.indexmundi.com/commodities/?commodity=shrimp&months=360
https://ourworldindata.org/seafood-production
https://www.cfec.state.ak.us/pmtvalue/X_S03T.HTM
http://www.adfg.alaska.gov/sf/FishCounts/
http://www.adfg.alaska.gov/index.cfm?ADFG=fishingCommercialByArea.main
http://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmonforecast
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_wholesale
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_statewide
https://www.adfg.alaska.gov/index.cfm?adfg=fishlicense.coar_salmonproduction
http://www.adfg.alaska.gov/sf/FishCounts/
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmon_grossearnings_byarea
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmon_by_report_type
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmon_combined_historical
https://www.adfg.alaska.gov/index.cfm?adfg=commercialbyfisherysalmon.salmoncatch_wholesale
