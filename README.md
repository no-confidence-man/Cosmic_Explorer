This is an API for Cosmic Explorer site evaluation, developed for ArcGIS in Python. 

You will have to pip install or conda install arcgis arcgis-mapping before running the code. 

Start with the file titled "setting_up." There are two ways of logging into your ArcGIS online account, and the comments in "setting_up" will walk you through it. The code in "setting_up" will to convert the KML files of the Cosmic Explorer sites to hosted feature layers, and publish them to your ArcGIS Online web map. KMLs must be converted to feature layers for ArcGIS to run any spatial analysis on them.

The file titled "buildings_and_kml_filtering" will identify, count, and extract the coordinates of all the buildings within a certain distance of the two x- and y-arms that compose a site. The output will include two csv files, one with just the building counts for each site within a KML file, and another with both counts and coordinates for all the buildings near a site. Then, the code will filter the original KMLs down to include only those sites that have zero buildings nearby, after which it will output another csv of the total sites and sites with zero buildigns for each KML.

The file titled "mapping_roads" will output a csv with the kilometers of roads within a certain radius of the three end stations (the x-end, y-end, and corner station) of each site.

You will see that my code often generates "buffers" and publishes them to your web map. Essentially, the buffer you define will be the area of interest within which all your buildings and road data will be collected. 
