# GIS on your phone

Your smartphone can do GIS!
This course teaches you how.

[you do need a smartphone - sorry!]

Android is preferred.
All apps are free.


### classes

1. take back your data!
  1. download your Google Location History at [Google Takeout](https://www.google.com/settings/takeout)
  1. convert to GeoJSON
  1. examine attributes, map 
1. GPX art
  1. go to [geojson.io](http://geojson.io/)
  1. digitize and download a vector layer that you will walk along in real life
  1. get [geopaparazzi](https://geopaparazzi.github.io/geopaparazzi/)
  1. go outside
  1. start recording GPS
  1. walk the vector you digitized
  1. stop recording GPS
  1. export geojson from geopaparazzi
  1. map both on [CartoDB](https://cartodb.com/) using torque
1. crowdsource streetview
  1. get [Mapillary](http://mapillary.com/)
  1. start taking photos
  1. upload and check
1. understand OSM community expectations
  1. community editing [good](http://wiki.openstreetmap.org/wiki/Good_practice) [practice](http://wiki.openstreetmap.org/wiki/Editing_Standards_and_Conventions)
  1. learn about how to use tags with [taginfo](http://taginfo.openstreetmap.org/) and the [wiki](http://wiki.openstreetmap.org/wiki/Highway_tagging_samples)
  1. basic rules
    1. "be bold" - but . . . 
    1. "map what's on the ground"
    1. only map what is verifiable: "another mapper should be able to come to the same place and collect the same data"
    1. nothing that *used* to exist, only things that exist *now*
      1. check out openhistoricalmap.org if you want stuff that used to be there but isn't anymore
    1. one feature per OSM element
      1. for example, a given restaurant appears exactly once, as it verifiably appears on the ground. A building footprint is good, but it should not also have a centroid feature with the name on top of its building footprint.
    1. It is best to map in person with a GPS. Aerial imagery is often deceitful because . . .
      1. it may suffer from position error greater than that of GPS
      1. imagery is often old.  The world changes and OSM should be up to date.
      1. building footprints have to be moved to the actual base of the building.  In other words, compensate for the angle at which the imagery was captured.
1. [MapGive](http://mapgive.state.gov/) - contribute to OpenStreetMap (not mobile)
  1. take the iD editor [tutorial](http://ideditor.com/)
  1. go to http://mapgive.state.gov/
  1. select a project
  1. use the HOT OSM tasking manager
1. [OsmAnd](http://osmand.net/) or [Vespucci](http://wiki.openstreetmap.org/wiki/Vespucci) - contribute to OpenStreetMap (mobile)
  1. get OsmAnd ( or Vespucci )
  1. go outside
  1. contribute to OSM
1. offline web map tiles
  1. OsmAnd ( offline tile download limit )
  1. gvSIG mobile ( no download limit! )
1. get custom MBTiles on your phone!
  1. get historical map or aerial photo of your area
  1. georeference that map using control points in QGIS
  1. use gdal2tiles.py on it to make a directory of web map tiles
  1. use mbutil on output directory of tiles to make an MBTiles file
  1. load MBTiles file into your phone and display in geopaparazzi
  1. go outside and visit historical places using your custom web map tiles as context!
  1. take photos of these places on Mapillary
1. contribute to OpenHistoricalMap!
  1. load the MBTiles of a historical map or aerial photo you made earlier for geopaparazzi
  1. open JOSM
  1. install the MBTiles plugin
  1. load your own MBTiles file into JOSM ( alternate method is to load image directly )
  1. change the API connection parameter to http://www.openhistoricalmap.org/api/ so we contribute to openhistoricalmap.org
  1. start digitizing features like roads and buildings and provide tags using your MBTiles for context ( can be as simple as building=yes )
  1. upload changes to OpenHistoricalMap!
1. get custom SpatiaLite database into your phone!
  1. in QGIS, convert the vector contributions you made to OpenHistoricalMap into a SpatiaLite database (just a single file with your layers!)
  1. in geopaparazzi, load the MBTiles you made earlier of a historical map or aerial photo
  1. in geopaparazzi, load the SpatiaLite database you just made of your OpenHistoricalMap contributions
  1. go outside
  1. as you explore, open Mapillary and take photos of places that have changed, for example buildings that are no longer there


### Resources


#### mobile

* [Mapillary](http://mapillary.com/)
  * take geotagged photos to build an open source street view
* [geopaparazzi](https://geopaparazzi.github.io/geopaparazzi/)
  * overlay your own . . .
    * MBTiles files
      * your own web maps!
    * GPX tracks
      * vector!
    * SpatiaLite layers
      * raster and vector in a SQL database!
    * or load a web map tile source by URL
      * but seriously you want to take advantage of that offline goodness
  * digitize!
  * take photos and notes!
    * but you should really be taking your photos with Mapillary
  * record GPX!
* MapBox
  * for iOS only - the Android one just displays web map tiles for now


#### on the web

* [geojson.io](http://geojson.io/)
  * digitize vectors, upload, add attributes, and share
* [MapBox](https://www.mapbox.com/)
  * MapBox Studio - vector tile styling
  * [TileMill](https://www.mapbox.com/tilemill/) - still awesome for making MBTiles files
* [CartoDB](https://cartodb.com/)
  * easiest possible way to make a web map
    * even animate with torque if you have a timestamp field
* [uMap](http://umap.openstreetmap.co/en/)
  * easy web maps
* [geocolor.io](http://geocolor.io/)
  * like geojson.io but for choropleth maps
* [OSRM](http://project-osrm.org/)
  * routing with OpenStreetMap


#### utils of awesome

  * [geojson-merge](https://github.com/mapbox/geojson-merge)
    * exactly what it says.  love that.
  * [geojson-join](https://github.com/tmcw/geojson-join)
    * join tables like CSV to geojson files
  * [mbutil](https://github.com/mapbox/mbutil)
    * make MBTiles web map tiles from any raster
      * (with gdal2tiles.py)
  * [mapshaper](https://github.com/mbloch/mapshaper) 
    * your topologically aware friend


#### reference

* [mapschool.io](mapschool.io)
  * what's GIS? with pictures.
* [mapmakers-cheatsheet](https://github.com/tmcw/mapmakers-cheatsheet)
  * should I make a map?  if so, how should I style it?
* [epsg.io](epsg.io), [epsg-registry](http://www.epsg-registry.org/)
  * what's my projection?  what projection should I use?
* [simple open data](http://simpleopendata.com/)
  * how to do open (geo) data
* [semantic versioning](http://semver.org/)
  * understand how to assign version numbers to your code and data


#### devices

* [riffle](http://openwaterproject.io/)
  * water monitoring in an old plastic bottle
* [infragram](http://openwaterproject.io/)
  * ground level remote sensing with a modded camera
* [mapknitter](http://mapknitter.org/)
  * mosaic and orthorectify aerial photos you take!


#### The Importance of Being Social
##### ( a trivial task for serious people )

* github
  * latest most awesome code
* twitter
  * latest news about all the coolest tools and people, and how and why they do their work

twitter handles to follow
* @Mapbox
* @mapillary


#### talks to pay attention to

* http://www.macwright.org/presentations/
* https://github.com/morganherlocker/talks
