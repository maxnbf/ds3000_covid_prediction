# Predicting COVID-19 Case Count Based on Prior Factors
## DS 3000 Summer 1 2020 Final Project
### By Luca Demian and Max Breslauer-Friedman

This is our repository for all our final project stuff.

### Useful Links

- FP2: [/data/](/data/)

### Description

For our project, we wanted to do something using COVD-19 data. At first, we were thinking of different unsupervised
project ideas about analyzing the factors which contributed to the pandemic spread in the United States. After review
we switched to thinking of supervised learning problems, and decided to attempt to develop a model to predict COVID-19
case count in a particular county based on several prior factors we identified. We decided to look at case count N days
after the first case recorded, to control for how the infection appeared non-uniformly throughout the states. We are
going to examine several different timelines, or N-day values.

### Data Sources

|Data Source|Link(s)|Date|Features|
|-|-|-|-|
|NY Times|[Link](https://github.com/nytimes/covid-19-data/blob/master/us-counties.csv)|May 22, 2020|`date_0days`, `cases_0days`, `deaths_0days`, `date_90days`, `cases_90days`, `deaths_90days`, `fips`
|Kaiser Health|[Link](https://khn.org/news/as-coronavirus-spreads-widely-millions-of-older-americans-live-in-counties-with-no-icu-beds/#lookup)|March 30, 2020|`icu_beds`, `kaiser_total_population`, `kaiser_60plus_population`
|US Census Commuting Data|[Link](https://www.census.gov/data/tables/2015/demo/metro-micro/commuting-flows-2015.html)|2015|`commuting_within`, `commuting_out`, `commuting_in`
|US Census Population Density|[Link](https://api.census.gov/data/2019/pep/population?get=DENSITY,POP&for=county:*)|2019|`density`, `pop_2019`
|Political Majority|[Link](https://github.com/tonmcg/US_County_Level_Election_Results_08-16/blob/master/2016_US_County_Level_Presidential_Results.csv)|2016|`percent_democrat`, `percent_gop`
|Poverty Data|[Link](https://www.ers.usda.gov/data-products/county-level-data-sets/download-data/)|Feb. 5, 2020|`percent_in_poverty`
|Age Data|[Link](https://data.census.gov/cedsci/table?q=Older%20Population&hidePreview=true&t=Older%20Population&tid=ACSDP1Y2018.DP05&vintage=2018&g=0100000US.050000)|2018|`pop_under18`, `pop_over65`, `pop_2018`, `median_age`
