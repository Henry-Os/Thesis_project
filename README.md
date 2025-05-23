## Estimating Optical Vegetation Indices (VIs) Using SAR Data for Crop Monitoring
This project uses SAR data from Sentinel-1 to estimate optical VIs from Harmonized Landsat Sentinel data (HLS). To improve model transferability across different geographical regions, time-related variables such as accumulated growing degree days (AGDD) and day-after-planting (DAP) are evaluated in addition to SAR variables and auxiliary data on a multi-seasonal time series data. Model performance is also assessed at different crop growth stages/VIs ranges. Corn and soyabeans are the 2 crops used in this project.

## Data Sources
[1. Harmonized Landsat Sentinel](https://search.earthdata.nasa.gov/search?q=hls)

[2. Sentinel-1](https://browser.dataspace.copernicus.eu/?zoom=13&lat=42.41262&lng=-85.39295&themeId=DEFAULT-THEME&visualizationUrl=U2FsdGVkX1%2FXhJJpN%2BOYbLs1%2Fznr5%2B192Z8L4Hq%2FxzRIS%2BSvycfw3t%2BmhJ4FFr%2BVEW4JNndTncyIoqx67O8XKysI05tWWdQKVxiXWDKInAhwniZv%2B0%2FFaiRkYyi1UmO%2F&datasetId=S2_L2A_CDAS&fromTime=2022-04-30T00%3A00%3A00.000Z&toTime=2022-04-30T23%3A59%3A59.999Z&layerId=1_TRUE_COLOR)

[3. ERA5 Surface Temperature for AGDD](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=download)

[4. Crop field boundaries for USA regions](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/index.php)

[5. Crop field boundaries for France region](https://geoservices.ign.fr/rpg)

[6. Crop field boundaries for Brazil region](https://ieee-dataport.org/open-access/campo-verde-database)

[7. DEM](https://www.usgs.gov/centers/eros/science/usgs-eros-archive-digital-elevation-shuttle-radar-topography-mission-srtm-1)

## Runing the code
All the optical and SAR data were preprocessed using the ESA SNAP software.
1. Part A imports the preprocessed satellite data, averages the satellite data response for each field boundary, and stores them as a geoparquet file for the analysis.
2. Part B imports the geoparquet file from file A, in addition to the temperature data for all regions. It cleans the data, creates features, trains and test models, and visualizes the results.
   
NB: To run Part A, you'll need to download all satellite data from the sources provided and preprocess them. 

