# Grassland-Management-Under-Climate-Change-Final
Taylor O'Brien's final project for Earth Analytics Data Bootcamp.

-Insert instructions-

## Grassland Management Under Climate Change

-Insert introduction for grassland and climate change

Grassland's are changing across the United States as climate change alters growing conditions. 

For this project, I will be taking two grasslands within the state of Colorado to look at the suitability of the grass, S. Nutans. I will be creating a suitability model for S. Nutans in both grasslands under RCP 4.5 and RCP 8.5 in the year 2050. These are the steps taken below to complete the model:
- Downloaded, reprojected, and clipped pH, elevation, and climatology data. 
- Calculated aspect from elevation
- Assigned a value of 1 to the most desirable climate variables for S. Nutan growing, with the rest of the values scaling down to 0
- Multiplying these rasters to plot a map with suitability for S. Nutans in the grassland

### Data Description

soil: Soil pH data between 0-5 cm, downloaded from POLARIS, with a resoltuion of 30 m is used in this final project. It is constructed using geospatial environmental data and a machine learning algorithm. 

elevation: The NASA Shuttle Radar Topography Mission (SRTM) dataset is used for elevation data. The purpose of SRTM is to generate a near-global digital elevation model (DEM) of the Earth using radar interferometry. Stated on NASA's website, "SRTM collected data in swaths, which extend from ~30 degrees off-nadir to ~58 degrees off-nadir from an altitude of 233 kilometers (km). These swaths are ~225 km wide, and consisted of all land between 60° N and 56° S latitude."

climate: 

### Citation

Soil: Chaney, N. W., Wood, E. F., McBratney, A. B., Hempel, J. W., Nauman, T. W., Brungard, C. W., & Odgers, N. P. (2016). POLARIS: A 30-meter probabilistic soil series map of the contiguous United States. Geoderma, 274, 54–67. USGS Publications Warehouse. https://doi.org/10.1016/j.geoderma.2016.03.025

Elevation: NASA JPL (2013). <i>NASA Shuttle Radar Topography Mission Global 1 arc second</i> [Data set]. NASA EOSDIS Land Processes Distributed Active Archive Center. Accessed 2023-12-04 from https://doi.org/10.5067/MEaSUREs/SRTM/SRTMGL1.003

Climate: 

### Model Description

For this assignment, I am implenting a fuzzy logic model. S Nutans is adapted to deep, moist soils with a pH range of 4.8 to 8.0. It has a medium tolerance to salinity and drought (USDA, NRCS 2017; Schmer et al. 2012).

S. Nutans grow in these conditions:

- pH= 4.8-8.0, for the purpose of this project I will be calculating the model using 6.5 as ideal conditions
- aspect= direct sunlight, for the purpose of this project I will be using south facing (180) as ideal conditions
- precip= 11-45 in, for the purpose of this project I will be calculating the model using 24 in as ideal conditions

All ideal conditions were assigned a value of 1, with all other values scaling down to 0. After pH, aspect, and precipitation are assigned these values, the 3 rasters are multiplied to show varying suitability within the grassland. In this model, we are looking at RCP 4.5 and RCP 8.5 for the year 2050. This model displays the suitability for S. Nutans to survive in Pawnee National Grassland and Cimarron National Grassland in the year 2050 under two different climate scenarios.
***
### References

Schmer, M., Q. Xue, and J. Hendrickson. 2012. Salinity effects on perennial, warm season (C4) grass germination adapted to the northern great plains. Can. J. Plant Sci. 92:873-881.

USDA, NRCS. 2017. The PLANTS Database (http://plants.usda.gov, 19 July 2017). National Plant data Team, Greensboro, NC 27401-4901 USA.