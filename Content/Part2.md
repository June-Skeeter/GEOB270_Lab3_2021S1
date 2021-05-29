---
layout: default
title: Identify and Acquire Data
nav_order: 3
---

# Acquire Data

## Data from the City

Port Alberni has provided you with four shapefiles and two text files that will be needed for the analysis:
* CityBoundaries.shp - Delineates the city boundaries
* Properties.shp - The boundaries and ZoneCode of all properties in Port Alberni
* Sirens.shp - The coordinates of the tsunami warning sirens
* Waterbodies.shp - The boundary of the water bodies in and around the city.
* Shelters.csv - Text file with the Lat/Lon coordinates of the tsunami warning shelters.
* ZoningCodes.csv - Text file with the 

**1)** Create a feature dataset in your Lab3_Project.gdb
* Creating a feature dataset will help you ensure all your input vector data is in the correct projection.
* Name the Feature Dataset "PA_Risk_Assessment"
* Set the coordinate system to NAD 1983 BC Environment Albers
	* The BC Albers is an equal area projection!
	* Set the coordinate system as a favorite so you can easily find it later.
<img src="BC_lbers.png" alt="hi" class="inline"/>

**2)** Import the four shapefiles from the PA_Data file into PA_Risk_Assessment feature dataset.


## Question 4)
Why are we creating a feature dataset to contain our input layers?
A) No reason
B) So everything is neatly grouped in one folder
C) To ensure all our vector data is in the same projection, the feature dataset will automatically re-project our vector data when importing
D) To ensure all our vector and raster data is in the same projection, the feature dataset will automatically re-project our vector and raster data when importing

<!-- C -->

The city hasn’t given you all the data you need to address the questions they’ve asked.  We need to retrieve some more layers to complete the project.

## Downloading Census Data

We need to download Dissemination Area level population data for the Port Alberni [census agglomeration](https://www150.statcan.gc.ca/n1/pub/92-195-x/2011001/geo/cma-rmr/cma-rmr-eng.htm) area using Simply Analytics.  You have access to this platform through the [UBC library](https://www.library.ubc.ca/).  Find the platform through the library web page, create an account, and sign in.

**1)** Download dissemination area (DA) level population data for the Port Alberni Census Agglomeration area.
* Create a new project.
* Search locations for th Port Alberni, BC (CMACA) layer
* Under Data, choose #Basics Population 2016.
* Under View Actions > Export and download the shapefile. 

**2)** Import the data into your feature dataset
* Once you have downloaded the census data layer, import it into your feature dataset.
* The file name from simply analytics isn't very descriptive.  Rename the layer to "Population_DA"

<iframe width="560" height="315" src="https://www.youtube.com/embed/gX8AZbZq9Og" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Question 5)
What is the difference between a Census metropolitan and a census agglomeration area?  See the link above for details?

<!-- CMA is for dense metro 100,000+, CA is less dense area 10,000+ -->


## Download a DEM from Google Earth Engine

We're going to download the [Canadian Digital Elevation Model](https://developers.google.com/earth-engine/datasets/catalog/NRCan_CDEM#description) (CDEM) from Google Earth Engine.  

**1)** Open the GEE Code editor and explore the CDEM.
* Use the link above to access the docs page for CDEM.  Midway down the page you will see some sample code and an option to Open the code Editor.
	* Open the sample code they provide.
	* Run it and see what happens.
<img src="GEE.png" alt="hi" class="inline"/>

* Change the coordinates of the Map.setCenter command to (-124, 49, 10).
	* -124, 49 are longitude and latitude, 10 is the "zoom level" for the display.

**2)** Download the DEM for the area around Port Alberni.
* In addition to uploading boundary files, you can define geometries (eg. a Rectangle) to download the data for a specific area.
* Copy and paste the code below at the end of the code.
	* Run it and use the same process as in Lab 2 to download the data and put it in your Lab3_Project
	* *Hint* Click Tasks in the top right and run the download.
* If you'd like to save this script for future use (ie. a final project), click save to save a copy of the layer.

```javascript
var Rect = ee.Geometry.Rectangle([-125,49, -124.5 ,49.5]);

Export.image.toDrive({
  image: elevation.mean(),
  description: 'PA_DEM',
  scale: 30,
  region: Rect
});
```

**3)** Re-project the PA_DEM and save it in your Lab3_Project.gdb
* Search for the Project Raster tool.
* Set PA_DEM as the input.
* Set the coordinate system to BC Albers
* Name the layer PA_DEM_Project and save it in your Lab3_Project.gdb

<img src="PA_DEM.png" alt="hi" class="inline"/>

## Downloading Roads Data from DataBC

To conduct the analysis, we’ll also need a roads layer.  This data set is available for download from [DataBC](https://www.data.gov.bc.ca/).  Follow the video instructions to inspect the metadata and request a download. 

**1)** Follow the link and download the roads layer.
* In the Search bar, type “Roads”.
    * Select “Digital Road Atlas (DRA) - Master Partially-Attributed Roads”
	* Whenever downloading data, it is crucial to check the metadata
    * Check your email for the download link (this may take a few minutes).
**2)** Download the data and add it to your PA_Data folder in your PA_RiskAssesment project.
* The layer name isn't very descriptive.  Name it PA_Roads

<iframe width="560" height="315" src="https://www.youtube.com/embed/5jaULGb5ux4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

**3)** Extract the .zip files from DataBC and import them into your PA_Risk_Assessment feature dataset
* The file names from DataBC aren't very descriptive, it might be helpful to change rename them "Roads" and "Coastline".

<img src="Roads.png" alt="hi" class="inline"/>
