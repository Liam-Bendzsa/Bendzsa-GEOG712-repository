# Global temperature anomalies by El Niño and La Niña conditions - Data package

This data package contains the data that powers the chart ["Global temperature anomalies by El Niño and La Niña conditions"](https://ourworldindata.org/grapher/global-temperature-anomalies-by-el-nino-la-nina?v=1&csvType=filtered&useColumnShortNames=false) on the Our World in Data website.

### Active Filters

A filtered subset of the full data was downloaded. The following filters were applied:

## CSV structure

Each row is an observation for an entity (usually a country or region) at a timepoint.

- "Entity" — the name of the entity, e.g. "United States".
- "Code" — our internal entity code. For most countries this is the [ISO alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code, e.g. "USA"; historical and other non-standard entities get a custom code.
- "Year" or "Day" — the timepoint. Annual data has a "Year" column holding an integer year; otherwise a "Day" column holds a date string in the form "YYYY-MM-DD".
- Every remaining column is a data column, each one a time series. Downloaded with the "full data" option each corresponds to one time series below; with "only selected data visible in the chart" they are transformed depending on the chart type, so the correspondence may be less direct.


## Metadata.json structure

The .metadata.json file contains metadata about the data package. The "charts" key contains information to recreate the chart, like the title, subtitle etc. The "columns" key contains information about each of the columns in the csv, like the unit, timespan covered, citation for the data etc.

## How we process data at Our World in Data

Our World in Data is almost never the original producer of the data - almost all of the data we use has been compiled by others. If you want to re-use data, it is your responsibility to ensure that you adhere to the sources' license and to credit them correctly. Please note that a single time series may have more than one source - e.g. when we stitch together data from different time periods by different producers or when we calculate per capita metrics using population data from a second source.

Preparing this data involves several processing steps. Depending on the data, this can include standardizing country names and world region definitions, converting units, calculating derived indicators such as per capita measures, as well as adding or adapting metadata such as the name or the description given to an indicator.
[Read about our data pipeline](https://docs.owid.io/projects/etl/).

## Detailed information about each time series


### Temperature anomaly
Difference of a specific month's average surface temperature from the 1991-2020 mean, in degrees Celsius.
Last updated: October 12, 2026  
Unit: °C  
Source: Contains modified Copernicus Climate Change Service information (2026) – with major processing by Our World in Data  

#### How to cite this data

Contains modified Copernicus Climate Change Service information (2026) – with major processing by Our World in Data

#### Notes on our processing step for this indicator
- Temperature measured in kelvin was converted to degrees Celsius (°C) by subtracting 273.15.

- Initially, the temperature dataset is provided with specific coordinates in terms of longitude and latitude. To tailor this data to each country, we utilize geographical boundaries as defined by the World Bank. The method involves trimming the global temperature dataset to match the exact geographical shape of each country. To correct for potential distortions caused by the Earth's curvature on a flat map, we apply a latitude-based weighting. This step is essential for maintaining accuracy, especially in high-latitude regions where distortion is more pronounced. The result of this process is a latitude-weighted average temperature for each nation.

- It's important to note, however, that due to the resolution constraints of the Copernicus dataset, this methodology might not be as effective for countries with very small landmasses. In these cases, the process may not yield reliable data.

- The derived 2-meter temperature readings for each country are calculated based on administrative borders, encompassing all land surface types within these defined areas. As a result, temperatures over oceans and seas are not included in these averages, focusing the data primarily on terrestrial environments.

- Global temperature averages and anomalies are calculated over all land and ocean surfaces.
- The temperature anomaly is calculated by comparing the average surface temperature of a specific time period (e.g., a particular year or month) to the mean surface temperature of the same period from 1991 to 2020.

- When calculating anomalies for each country, the average surface temperature of a given year or month is compared to the 1991-2020 mean temperature for that specific country.

- The reason for using the 1991-2020 period as the reference mean is that it is the standard reference period used by our data source, the Copernicus Climate Change Service. This period is also adopted by the UK Met Office. This approach ensures consistency in identifying climate variations over time.


### Oceanic Niño Index (ONI) anomaly
The Oceanic Niño Index (ONI) anomaly is a measure of the sea surface temperature anomalies in the east-central tropical Pacific Ocean.
Last updated: October 12, 2026  
Next expected update: November 2026  
Source: NOAA National Centers for Environmental Information (2026) – with minor processing by Our World in Data  

#### How to cite this data

NOAA National Centers for Environmental Information (2026) – with minor processing by Our World in Data

#### What you should know about this data
- The Oceanic Niño Index (ONI) is a tool used by the National Oceanic and Atmospheric Administration (NOAA) to monitor and track the presence and intensity of El Niño and La Niña events.
- These events are part of the broader El Niño-Southern Oscillation (ENSO), a natural climate pattern that affects global weather patterns, including rainfall, droughts, and hurricane activity.
- The ONI measures deviations in sea surface temperatures (SSTs) in a specific area of the Pacific Ocean, known as the Niño 3.4 region. This region spans from 120°W to 170°W longitude, along the equator, in the east-central tropical Pacific.
- NOAA calculates the ONI by taking a 3-month running mean of SST anomalies. An anomaly is the difference between observed SSTs and the 30-year climatological average for the same period. NOAA periodically updates the baseline period to ensure consistency with long-term climate trends. For example, the 1991–2020 average is often used.
- El Niño (ONI ≥ +0.5°C) occurs when sea surface temperatures in the Niño 3.4 region are warmer than usual, often bringing drier conditions to Asia and Australia, wetter weather to the southern United States, and weakened trade winds.
- El Niño can lead to weaker Atlantic hurricane seasons but stronger and more frequent Pacific hurricanes.
- Neutral (−0.5°C < ONI < +0.5°C) means sea surface temperatures are near average, with no significant ENSO event.
- La Niña (ONI ≤ −0.5°C) happens when sea surface temperatures are cooler than usual, often causing drier conditions in South America, increased rainfall in Indonesia and northern Australia, and stronger trade winds.
- La Niña tends to cause more hurricanes in the Atlantic and drought conditions in the southern U.S.

#### How this data is described by its producers
- El Niño (La Niña) is a phenomenon in the equatorial Pacific Ocean characterized by a five consecutive 3-month running mean of sea surface temperature (SST) anomalies in the Niño 3.4 region that is above (below) the threshold of +0.5°C (-0.5°C). This standard of measure is known as the Oceanic Niño Index (ONI).
- Historically, scientists have classified the intensity of El Niño based on SST anomalies exceeding a pre-selected threshold in a certain region of the equatorial Pacific. The most commonly used region is the Niño 3.4 region, and the most commonly used threshold is a positive SST departure from normal greater than or equal to +0.5°C. Since this region encompasses the western half of the equatorial cold tongue region, it provides a good measure of important changes in SST and SST gradients that result in changes in the pattern of deep tropical convection and atmospheric circulation. The criteria, that is often used to classify El Niño episodes, is that five consecutive 3-month running mean SST anomalies exceed the threshold.
- Studies have shown that a necessary condition for the development and persistence of deep convection (enhanced cloudiness and precipitation) in the Tropics is that the local SST be 28°C or greater. Once the pattern of deep convection has been altered due to anomalous SSTs, the tropical and subtropical atmospheric circulation adjusts to the new pattern of tropical heating, resulting in anomalous patterns of precipitation and temperature that extend well beyond the region of the equatorial Pacific. An SST anomaly of +0.5°C in the Niño 3.4 region is sufficient to reach this threshold from late March to mid-June. During the remainder of the year a larger SST anomaly, up to +1.5°C in November-December-January, is required in order to reach the threshold to support persistent deep convection in that region.
- SST values in the Niño 3.4 region may not be the best choice for determining La Niña episodes but, for consistency, the index has been defined by negative anomalies in this area. A better choice might be the Niño 4 region, since that region normally has SSTs at or above the threshold for deep convection throughout the year. An SST anomaly of -0.5°C in that region would be sufficient to bring water temperatures below the 28°C threshold, which would result in a significant westward shift in the pattern of deep convection in the tropical Pacific.


## Sources

These are the sources behind the data in this package. Each time series above names the ones it draws on in its citation.

### Contains modified Copernicus Climate Change Service information – ERA5 monthly averaged data on single levels from 1940 to present

ERA5 is the latest climate reanalysis produced by ECMWF, providing hourly data on many atmospheric, land-surface and sea-state parameters together with estimates of uncertainty.

ERA5 data are available in the Climate Data Store on regular latitude-longitude grids at 0.25° x 0.25° resolution, with atmospheric parameters on 37 pressure levels.

ERA5 is available from 1940 and continues to be extended forward in time, with daily updates being made available 5 days behind real time

Initial release data, i.e., data no more than three months behind real time, are called ERA5T.

Producer: Contains modified Copernicus Climate Change Service information  
Published: 2026-08-21  
Retrieved on: 2026-10-12  
Retrieved from: https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview  
License: Copernicus License (https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview)  

Citation: Hersbach, H., Bell, B., Berrisford, P., Biavati, G., Horányi, A., Muñoz Sabater, J., Nicolas, J., Peubey, C., Radu, R., Rozum, I., Schepers, D., Simmons, A., Soci, C., Dee, D., Thépaut, J-N. (2023): ERA5 monthly averaged data on single levels from 1940 to present. Copernicus Climate Change Service (C3S) Climate Data Store (CDS), DOI: 10.24381/cds.f17050d7 (Accessed on 21-August-2026)

### NOAA National Centers for Environmental Information – Equatorial Pacific Sea Surface Temperatures (SST) data

The dataset contains data on El Niño and La Niña, phenomena in the equatorial Pacific Ocean defined by a five consecutive 3-month running mean of sea surface temperature (SST) anomalies in the Niño 3.4 region. El Niño occurs when the anomalies exceed +0.5°C, while La Niña occurs when they fall below -0.5°C. This measure is known as the Oceanic Niño Index (ONI).

Producer: NOAA National Centers for Environmental Information  
Published: 2026  
Retrieved on: 2026-10-12  
Retrieved from: https://www.ncei.noaa.gov/access/monitoring/enso/sst  
Direct download: https://www.cpc.ncep.noaa.gov/data/indices/sstoi.indices  
License: CC BY 4.0 (https://gml.noaa.gov/about/disclaimer.html)  

Citation: National Oceanic and Atmospheric Administration (NOAA) National Centers for Environmental Information (NCEI) – Equatorial Pacific Sea Surface Temperatures (SST) data

    