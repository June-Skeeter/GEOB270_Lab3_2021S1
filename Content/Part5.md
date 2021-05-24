---
layout: default
title: Last Minute Changes
nav_order: 6
---

# Last Minute Changes

## Refining the Population at Risk Estimate
You’re taking a coffee break and you run into another colleague. They ask what you’ve been working on. You tell them about your project, and how your a bit troubled about your Population_at_Risk estimate. You’re concerned it wayyy to high, and the city won’t listen to your recommendations because you’re including any DA that even has a sliver in the Inundation_Zone.

Your college suggests one last step: “If you clip the Population_at_Risk layer by the residential properties Properties a Risk layer, you’ll ensure that you’re only including DAs that are in the Inundation Zone and contain properties that are at risk!”

You think … hmm … Its not the perfect solution. But it will work. It will still be an over estimate (which is better than an under estimate in this case), but it will do.

Add a select by attribute (select for the residential zone codes) the clip to your model, then run it again.

## Updated Projections
Just as you’re getting ready to make your maps, and write your report, you get a message on Slack from a colleague.  She tells you about a new modeling study that was just published suggests that peak wave height could be up to 15 meters and the wave could reach 1250m inland rather than 1000m.  Update your raster reclassification values and the coastline buffer distance to reflect this new information and rerun your model to update your analysis!

## Question 11)
What is the total shape_area of your InundationZone layer?
<!-- 12,602,728.8 -->

## Question 12)
This isn't the total area within the MunicipalBoundary that is at risk however.  Why?  What would you need do to figure out the total area within the MunicipalBoundary at risk?

## Share Your Model

Your supervisor wants to have a quick look at your workflow before you start to draft your report.  In your model window, hit Auto Layout one more time.  Then click export and save your model as PA_RiskAssesment.pdf  Note Make sure you save your output as a .pdf, not a .svg file!

## Question 13)
"Email" a copy of your workflow to your supervisor by uploading it here!
