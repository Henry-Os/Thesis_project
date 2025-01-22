## Optical vegetation indices (VIs) estimation project
This code uses SAR data from Sentinel-1 to estimate optical VIs from Harmonized Landsat Sentinel data (HLS). To improve spatial transferability across different geographical regions, time-related variables such as growing degree days (GDD) and day of year (DOY) are evaluated on a multi-seasonal time series data. Model performance is also assessed at different crop growth stages.

## Data Sources
[1. Harmonized Landsat Sentinel](https://search.earthdata.nasa.gov/search?q=hls)

[2. Sentinel-1](https://browser.dataspace.copernicus.eu/?zoom=13&lat=42.41262&lng=-85.39295&themeId=DEFAULT-THEME&visualizationUrl=U2FsdGVkX1%2FXhJJpN%2BOYbLs1%2Fznr5%2B192Z8L4Hq%2FxzRIS%2BSvycfw3t%2BmhJ4FFr%2BVEW4JNndTncyIoqx67O8XKysI05tWWdQKVxiXWDKInAhwniZv%2B0%2FFaiRkYyi1UmO%2F&datasetId=S2_L2A_CDAS&fromTime=2022-04-30T00%3A00%3A00.000Z&toTime=2022-04-30T23%3A59%3A59.999Z&layerId=1_TRUE_COLOR)

[3. Surface Temperature](https://www.ncei.noaa.gov/access/metadata/landing-page/bin/iso?id=gov.noaa.ncdc%3AC00861)

[4. Crop field boundaries for USA regions](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/index.php)

[5. Crop field boundaries for France region](https://geoservices.ign.fr/rpg)

[6. Crop field boundaries for Brazil region](https://ieee-dataport.org/open-access/campo-verde-database)

## Runing the code
All the optical and SAR data were preprocessed using the ESA SNAP software.
1. Part A imports the preprocessed satellite data, averages the satellite data response for each field boundary, and stores them as a geoparquet file for the analysis.
2. Part B imports the geoparquet file from file A, in addition to the temperature data for all regions. It cleans the data, creates features, trains and test models, and visualizes the results.
   NB: To run Part A, you'll need to download all satellite data from the sources provided and preprocess them. 

