---
layout: default
title: Parse Data
nav_order: 3
---

# Parse Data

## Polyline to Polygon

You have a CityBoundaries shapefile. We’re going to use the city boundary to clip our other data layers to the area just around the city.  You can think of clipping as a “cookie cutter” all the areas of one layer that are contained within the boundaries of another layer are kept.  All the areas outside the bounds are discarded.  Clipping is a way to cut down on the size of a dataset.
    Add the CityBoundaries to your map. You might notice that this layer is just a polyline.  In order to use it for a clip, we need to create a polygon.
    Follow the video instructions to convert from a polyline to a polygon. (Links to an external site.)
      
    You can also reference this link. (Links to an external site.)
    When you’re done creating the MunicipalBoundary polygon, make sure to save your edits (click Save in edit tab)!
Looking at the municipal boundary, you’ll notice its irregularly shaped. For instance, the Ahahswinis Reserve is not within the city boundary; however we want to make sure its included in our risk assessment, along with other areas just beyond city limits.
    To make sure we include the adequate areas, we’re going to buffer the MunicipalBoundary by 1km.
    Follow the video instructions to conduct the buffer. (Links to an external site.)
     
    You can also reference this link. (Links to an external site.)

## Clip the Data.
The next step is to clip the rest of the data layers by the boundaries of the MunicipalBoundary_Buffer
    The tsunami warning towers and the Waterbodies are already only within the study area so we don’t need to worry about them.
    We need to clip the Population_DA.shp, the roads and PA_DEM.tif to “cut them down to size”..
    Follow the video instructions to clip both vector and raster layers. (Links to an external site.)
     
    You can also reference this link for clipping vectors  (Links to an external site.)and this one for clipping rasters. (Links to an external site.)

## Display XY Data
You’ll notice Shelters.csv is not a shapefile. .csv files are not spatial data and cannot be drawn on the map. This a .csv file that was created by the city, listing the proposed locations (in Latitude & Longitude) of potential shelters.

    You can’t directly draw .csv files in Arc, but when working with point data, you can import and Display XY Data stored in a .csv file. Since this data is in latitude & longitude you will also need to reproject it.
    Follow the video instructions to display XY data and reproject.  (Links to an external site.)
     
    You can also reference this link (Links to an external site.) and this link. (Links to an external site.)
    You may want to consider renaming this layer to something more descriptive like “Shelters"
    *Note the final positions of one of the Shelters has changed since I recorded this video.  Don't worry if one of your shelters doesn't match up with the example


