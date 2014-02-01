# SLIP Future and Desktop GIS
If you're using desktop GIS applications and WFS to access SLIP data already there are a few differenes you should be aware of as you're switching over to SLIP Future.

* WFS services are provided as WFS 2.0 - WFS 1.0.0 and 1.1.0 aren't available.
* WFS services in SLIP Future contain only a single layer. i.e. There's one Cadastre (Polygons) service, one LGA Boundaries service, et cetera. This is a function of how Google has implemented WFS (as a layer on top of the GME API).
* There are no longer feature limits on WFS requests. Instead requests use the WFS 2.0 concept of 'pages' to provide results 1,000 features at a time along with a *nextPageToken* to the next page in the request.

The impact of these changes will vary depending on how you were using WFS in SLIP Classic.

## I just want to view the data in my favourite desktop GIS package


## I was using WFS to download and locally cache data from SLIP Classic


# QGIS
### WFS

### Google Maps Engine Plugin


# ArcGIS
### WFS

### Google Maps Engine Plugin


# FME


@TODO How to install and use QGIS plugin https://docs.google.com/document/d/1b-FQS0O1q9y-RJxCk-oZTqbmryZSLYnago9lzCatjIY/edit#heading=h.y1c7y14dgynv
@TODO Google ArcGIS doco https://docs.google.com/file/d/0B0kxJh5jFHnycGRuRnZLRHQ5d28/edit
@TODO Google QGIS doco https://docs.google.com/file/d/0B0kxJh5jFHnySjdqcklmSVZNRDQ/edit
@TODO Link to GitHub for each + any Google blog posts about them (?)
@TODO WFS2 in QGIS, ArcGIS
@TODO New FME stuff
@TODO Note WFS 1 bridge investigations
