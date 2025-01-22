## Optical vegetation indices (VIs) estimation project
This code uses SAR data from Sentinel-1 to estimate optical VIs from Harmonized Landsat Sentinel data (HLS). To improve spatial transferability across different geographical regions, time-related variables such as growing degree days (GDD) and day of year (DOY) are evaluated. Model performance is also assessed at different crop growth stages.

## Data Sources
[1. Harmonized Landsat Sentinel](https://search.earthdata.nasa.gov/search?q=hls)
[2. Sentinel-1](https://browser.dataspace.copernicus.eu/?zoom=13&lat=42.41262&lng=-85.39295&themeId=DEFAULT-THEME&visualizationUrl=U2FsdGVkX1%2FXhJJpN%2BOYbLs1%2Fznr5%2B192Z8L4Hq%2FxzRIS%2BSvycfw3t%2BmhJ4FFr%2BVEW4JNndTncyIoqx67O8XKysI05tWWdQKVxiXWDKInAhwniZv%2B0%2FFaiRkYyi1UmO%2F&datasetId=S2_L2A_CDAS&fromTime=2022-04-30T00%3A00%3A00.000Z&toTime=2022-04-30T23%3A59%3A59.999Z&layerId=1_TRUE_COLOR)
[3. Surface Temperature](https://www.ncei.noaa.gov/access/metadata/landing-page/bin/iso?id=gov.noaa.ncdc%3AC00861)
[4. Crop field boundaries for USA regions](https://www.nass.usda.gov/Research_and_Science/Crop-Sequence-Boundaries/index.php)
[5. Crop field boundaries for France region](https://geoservices.ign.fr/rpg)
[6. Crop field boundaries for Brazil region](https://ieee-dataport.org/open-access/campo-verde-database)

