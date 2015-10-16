OpenCube MapView
===============

The OpenCube Map View enables map-based visualizations of linked data cubes with a geo-spatial dimension. It enables performing OLAP operations. 

### How it works

The OpenCube MapView is developed as a separate component of the OpenCube toolkit and is part of the “Data Exploring” lifecycle step. It supports visualization of cubes containing a geospation dimension (i.e. sdmx-dimension:refArea). The MapView can be initialized by creating a widget giving as input the map focus to be used (currently BE and EU are supported). The visualization maps are created using OpenStreetMap.

Widget configuration:
```
{{#widget: MapView|
      asynch='true' |
      mapzoom='BE'
 }}
```   

###Functionality

Currently the maps supported by MapView are:
+ **Choropleth map**. Each location available in the dataset is represented as a polygon in the visualized map. The polygon changes color density depending on observation's measure value.
+ **Markers Map**. It. uses markers to represents the observation value for a specific geographic location for a combination of dimension restrictions. 
+ **Bubble Map**. Each bubble represents the observation value for a specific geographic location for a combination of dimension restrictions. The radius of the bubble indicates the value of the observation's measure. 


The functionalities that are provided by the OpenCube Map View regardless the type of the selected map are the following:

+ The user can change the type of visualization from a dropdown list.
+ The user can change the values of the fixed dimensions in the dropdown list.
+ The user can select the dimensions that will be included in the cube that will be visualized on the map.
+ The user can create and store an one-dimensional slice based on the data that are presented on the map.
+ The user can select the geography granularity to be visualized
 