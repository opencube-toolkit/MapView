OpenCube MapView
===============

The OpenCube Map View enables the visualization on a map of RDF data cubes based on their geospatial dimension

### How it works

The OpenCube MapView is developed as a separate component of the OpenCube toolkit and supports visualization of cubes containing a geospation dimension.
The MapView can be initialized by creating a widget giving as input the URI of the cube to be visualized and the map focus to be used (currently BE and EU are supported).

Widget configuration:
```
{{#widget: MapView|
      dataCubeURI= '<http://id.statistiek.vlaanderen.be/dataset/inburgering#id>' |
      asynch='true' |
      mapzoom='BE'
 }}
```   

###Functionality

Currently the maps supported by MapView are:
+ **Markers Map**. It. uses markers to represents the observation value for a specific geographic location for a combination of dimension restrictions. 
+ **Bubble Map**. Each bubble represents the observation value for a specific geographic location for a combination of dimension restrictions. The radius of the bubble indicates the value of the observation's measure. 
+ **Choropleth map**. Each location available in the dataset is represented as a polygon in the visualized map. The polygon changes color density depending on observation's measure value. 