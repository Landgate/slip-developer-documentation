# Google Maps Engine API
The GME API is a RESTful JSON API that provides read, write, and search capabilities to all of the assets in SLIP Future. Read access to the public datasets in SLIP Future is available to any Google account with an API key. Write operations, search queries, and access to subscripton datasets are limited to authenticated accounts that have been granted at least viewer-level access.

Retrieving data via the GME API is as simple as:

```
https://www.googleapis.com/mapsengine/v1/tables/{assetId}/features?version=published&key={yourapikey]
```

[Try it now]()

For the full list of functions available via the GME API see the [Google Maps Engine API Reference](https://developers.google.com/maps-engine/documentation/reference/v1/). To get started with the GME API see [Google's GME API Tutorial](https://developers.google.com/maps-engine/documentation/tutorial) and our own [code samples using SLIP Future]().

@TODO Try it now link
@TODO New project w/ limited QPD against something in Locate
@TODO Locate assetIds
@TODO Limits
@TODO How to get read access
@TOOD Code samples link


# Web Feature Services
Google Maps Engine provides a partial WFS 2.0 implementation for users who prefer or need to use OGC standard services to access vector data. For further information on the capabilities of WFS 2.0 see [this pdf]() and the [comparison chart]().

```
https://clients6.google.com/mapsengine/wfs_experimental/wfs/{assetId}/?REQUEST=GetCapabilities&SERVICE=WFS2.0&assetVersion=published
```

[Try it now]()

Users of desktop GIS applications should see our [SLIP Future and Desktop GIS]() page for instructions on how access SLIP Future in these applications. 

> **Note:** WFS is currently in beta and it is not recommend for use in production applications. When Landgate has provided sign off to Google on this implementation it will be elevated to released status.

@TODO Try it now link
@TODO WFS PDF link (OK?)
@TODO Comparison chart link - Separate WFS page?
@TODO Desktop GIS link

# Google Maps JavaScript API
The popular Google Maps JavaScript API provides a number of layers specifically for accessing data within a Google Maps Engine instance; including:

* Display any Google Maps Engine layer via the *MapsEngineLayer* class,
* Add interactive functions and customise the styling of a layer via the *DynamicMapsEngineLayer* class, and
* The *HeatmapLayer* class to visualise data intensity.

API documentation and demos can be found [here](https://developers.google.com/maps/documentation/javascript/visualization) and code samples based on data in SLIP Future can be found [here]().

@TOOD Code samples link


# Web Map (Tiling) Services
Google Maps Engine supports the WMS (1.1.1 & 1.3.0) and WMTS (1.0) standards for web mapping for all data in SLIP Future.

> WMS
```
https://mapsengine.google.com/{assetId}-4/wms/?REQUEST=GetCapabilities&VERSION=1.3.0
```

[Try it now]()

> WMTS
```
https://mapsengine.google.com/{assetId}-4/wmts/?REQUEST=GetCapabilities&VERSION=1.0
```

[Try it now]()

Web mapping libraries such as [OpenLayers](http://openlayers.org/) and [Leaflet](http://leafletjs.com/) provide integration with WM(T)S services and can easily be used to provide beautiful device-independent web maps using SLIP Future. Check out our [code samples]() to get started.

@TODO Try it now links
@TOOD Code samples link


# Google Earth
All map services in SLIP Future automatically provide access to KML feeds suitable for user of Google Earth.

> Google Earth KML
```
https://mapsengine.google.com/{assetId}-4/kmlmaplink/
```

[Try it now]()

> Google Earth DB Link
```
https://mapsengine.google.com/{assetId}-4/kh/
```

[Try it now]()

@TOOD Try it now links
