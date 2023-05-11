---
title: Heatmap - Connectivity
permalink: "/docs/heatmap-connectivity/"
sections:
- technical
weight: 60
---

#### Definition

Different indicators, such as a connectivity heatmap, serve as transport infrastructure planning benchmarks for network connectivity. This integrated feature in the GOAT allows us to measure street network connectivity. 

It can be computed for different transport modes and visualizes the area size of different isochrone intervals on the level of a hexagonal grid. By that, users can identify high on low-connected areas in the study area. Weak points in street connectivity can be easily identified and the degree of network connectivity for the whole study area be assessed.  

The connectivity heatmap is based on isochrone calculation, a method for computing travel time between different locations. Since this indicator is highly dependent on the isochrone feature, we strongly recommend reading the isochrone documentation first. Further information on the isochrone calculation can be examined [here.](/en/docs/isochrone/ "Indicator documentation on our isochrone") 


#### Routing Modes

Depending on the chosen travel mode GOAT uses different parts of the street network. To keep the platform flexible the street network categories can be adjusted to the local study context when setting up the tool.

Depending on the availability of data in the study area and the planning purpose different routing profiles are available. These are walking, cycling, pedelec and public transport.


#### 1. Walking

Default routing profile for walking, considering all paths accessible by foot.

Default walking speed: 5km/h

<img src="\images\docs\technical_documentation\isochrone\walking_en.webp" alt="walking isochrone" style="max-height:85px;"/>

#### 2. Cycling

#### 2.1 Standard

Default routing profile for cycling, considering all paths accessible by bicycle.

Default cycling speed: 15km/h Depending on the surface, smoothness and slope of the different street segments, the cycling speed is adjusted accordingly.

<img src="\images\docs\technical_documentation\isochrone\standard_en.webp" alt="standard isochrone" style="max-height:88px;"/>

#### 2.2 Pedelec

Same as the standard routing profile, but with an increased cycling speed of 23 km/h.
For Pedelecs, slopes are considered with a lower impedance than for Standard bicycles.

<img src="\images\docs\technical_documentation\isochrone\pedelec_en.webp" alt="pedelec isochrone" style="max-height:80px;"/>



#### What planning questions can be answered? 

  - How well is the study area's transportation infrastructure connected? 
  - Where are the network gaps? 
  - Where are the areas to be improved?
  - Where are the barriers for pedestrians in the context of street network connectivity? 
  - How does a new pedestrian bridge influence connectivity? 


#### Calculation

In GOAT, the connectivity heatmap is calculated using a hexagonal grid with an edge length of approximately 66 m per cell. 
You can check [here](https://h3geo.org/docs/core-library/restable "H3 Geo Documentation") for more details on hexagonal grids or further details on [H3 Grid.](/en/docs/glossary/#h-3-grid "Documentation Glossary") 

For each hexagon centroid, the reachable area is computed using an isochrone with the maximum travel time of the selected transportation mode. This calculation returns the travel time from the centroid to each pixel of the isochrone (as indicated in Figure 1 below), so the connectivity can be computed by summing up the pixels for each travel time (one-minute intervals) and dividing the sum by the maximum travel time (in Figure 2). 

<p align="center">
<img src="\images\docs\technical_documentation\connectivity\sketch_en.webp" alt="sketch travel time" style="max-height:380px;"/>
<p align="center">

_Figure 1: Travel time from the centroid to each pixel grid of the isochrone_


<img src="\images\docs\technical_documentation\connectivity\formula_en.webp" alt="formula" style="max-height:120px;"/>


_Figure 2: Formula of the average reached area_


The resulting connectivity values are classified into six levels, from highest to lowest  [as quintile classification.](/en/docs/glossary/#quintile-classification "Quintile Classification") This classification helps to identify areas with relatively small or large catchments, allowing to locate gaps in the network and potential areas for improvement. 


#### Visualization 

In GOAT, the connectivity heatmap is visualized using a hexagonal grid with an edge length of approximately 174 m per cell.

The classified hexagons are colored from **high** ( <span style="color:green">green </span>) to **low** ( <span style="color:red">red </span>) connectivity, giving the user a clear overview of the network quality throughout the study area for the different modes. 


<img src="\images\docs\technical_documentation\connectivity\connectivity_new_en.webp" alt="connectivity heatmap" style="max-height:450px;"/>


_Figure 3: Connectivity Heatmap in GOAT_