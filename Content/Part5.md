---
layout: default
title: Last Minute Changes
nav_order: 6
---

# Last Minute Changes

## Refining the Population at Risk Estimate
You’re taking a coffee break and you run into a colleague. They ask what you’ve been working on. You tell them about your project, and how your a bit troubled about your Population_at_Risk estimate. You’re concerned it wayyy to high, and the city won’t listen to your recommendations because you’re including any DA that even has a sliver in the Inundation_Zone.

Your college suggests one last step: “If you clip the Population_at_Risk layer by the residential properties Properties a Risk layer, you’ll ensure that you’re only including DAs that are in the Inundation Zone and contain properties that are at risk!”

You think … hmm … Its not the perfect solution. But it will work. It will still be an over estimate (which is better than an under estimate in this case), but it will do.

Add a select by attribute (select for the residential zone codes) the clip to your model, then run it again.

## Updated Projections
Just as you’re getting ready to make your maps, and write your report, you get a message on Slack from a colleague.  She tells you about a new modeling study that was just published suggests that peak wave height could be up to 15 meters and the wave could reach 1250m inland rather than 1000m.  Update your raster reclassification values and the coastline buffer distance to reflect this new information and rerun your model to update your analysis!

## Question 12)
What is the total shape_area of your InundationZone layer?

<!-- 16,219,855.5 -->

## Question 13)
This isn't the total area within the MunicipalBoundary that is at risk however.  Why?  What would you need do to figure out the total area within the MunicipalBoundary at risk?

<!-- Clip the inundation zone by the municipal boundary (not the buffered boundary!) -->

## Summarize Statistics for Your Report

Watch the video for pointers on summary tables.

<iframe width="560" height="315" src="https://www.youtube.com/embed/C--8LGmxe08" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## Question 14)
How many people within Port Alberni and the surrounding area are potentially living in areas at risk?

<!-- 6,474 -->

## Question 15)
How many residential properties are at risk?

<!-- 971 residential -->

## Question 16)
How many kilometers of arterial roadways are at risk for flooding?

<!-- 8.43238108989368 -->
<!-- 
I will determine a margin of error based on everyone's answers and give partial credit.  For now the margins have been set to zero, but that will change when we mark the lab. -->