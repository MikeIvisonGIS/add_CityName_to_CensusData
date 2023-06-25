# add_CityName_to_CensusData

### add_CityName_to_CensusData README

By: Michael Ivison

**Purpose of Program:** 

A project containing a jupyter notebook file used in ArcGIS Pro to merge two datasets and create a custom dataset containing the city boundary polygons to all cities in the United States.

Project uses pandas, geopandas functionality, and arcpy (Python).

For an outline, see the City_Boundaries_Project_Outline.docx file.

**Input Parameters:**

1) Spatial dataset - 2022 TIGER/Line Zip Code Tabulation Area
   Data Source: https://www.census.gov/cgi-bin/geo/shapefiles/index.php?year=2022&layergroup=ZIP+Code+Tabulation+Areas
2) Non-Spatial dataset - US States Cities Database
   Data Source: https://simplemaps.com/data/us-cities#zip_method

**Intermediate Parameters**

1) df_csv = pandas dataframe from US Citites .csv
2) df_new = truncated df_csv dataframe to contain ['city'] and ['zips'] columns
3) geo_df = geospatially enabled pandas dataframe on the 2022 TIGER/Line Zip Code Tabulation Areas shapefile (.shp)
4) df_merge = a merged dataset of df_new and geo_df
5) Updated TIGER/Line Zip Code Tabulation Areas shapefile (.shp) - tl_2022_us_zcta520_cities

**Output Parameters:**

1) US_City_Boundaries.shp - A shapefile of the city boundaries that result from the merge of the two datasets.
