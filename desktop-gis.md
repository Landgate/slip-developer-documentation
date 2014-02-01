# SLIP Future and Desktop GIS
If you are currently using desktop GIS applications - and WFS in particular - to access SLIP Classic already there are a few crucial differenes you should be aware of as you're switching over to SLIP Future.

1. WFS services are provided as WFS 2.0, not 1.0.0 and 1.1.0 as was the case in SLIP Classic.
> Landgate is looking at developing a 2.0 - 1.0 bridge - see below for further details.

2. There are no longer feature limits on WFS requests.
> Requests to retrieve vector features will now be 'paged' at up to 1,000 features/request, with each page containing a *nextPageToken* URI pointing to the next page in the request.

3. WFS services in SLIP Future contain only a single layer.
> e.g. There's one Cadastre (Polygons) service, one LGA Boundaries service, et cetera.

4. Authentication is handled via the OAuth 2.0 protocol, not the older HTTP Basic username + password method.
> OAuth 2.0 is an industry standard protocol with widespread adoption and amongst large websites and API providers. HTTP Basic, while a more convenient protocol for some users, is inherently much more insecure and is no longer recommend for use in modern applications. Find out more about [OAuth and Google Maps Engine](https://developers.google.com/maps-engine/documentation/oauth/).

## WFS Proxy
Google has developed a WFS Proxy application for Landgate that allows clients to connect using a username and password as is the case in SLIP Classic. In the longer-term we are keen to see OAuth 2.0 support added to desktop GIS packages, but until then Landgate will maintain the WFS Proxy.

*Details on how to sign up to and connect to the WFS Proxy are coming soon.*

## WFS 2.0 - 1.0 Bridge
Owing to the wide lack of WFS 2.0 support across desktop GIS packages Landgate are in the process of evaluating the development of a WFS 2.0 to WFS 1.0 bridge to provide backwards compatability with SLIP Classic.

More information will be available shortly.

## I was using WFS to download and locally cache data from SLIP Classic
The good news you now have two options (WFS 2.0 & the GME API) for downloading vector features *and* you're no longer subject to feature limits.

The less good news is that you will have to change your downloading scripts.

We're keen to work with advanced users to help you in understanding the changes and adapt your processes to using SLIP Future. To begin with check out our Getting Started $LINK$ page for an introduction to SLIP Future for programmers; and then visit our Code Samples $LINK$, where you'll find a couple of samples using the GME API to programatically download vector data.

## I just want to view data in a desktop GIS package
### QGIS
#### WFS
In QGIS 1.8.0+ the third-party **WFS 2.0 Client** plugin provides access to public WFS 2.0 services from SLIP Future.

[Plugin installation instructions](https://drive.google.com/file/d/0B0kxJh5jFHnyNndmSHdZRGtSb0k/edit?usp=sharing)

[Plugin homepage](http://plugins.qgis.org/plugins/wfsclient/)

> **Note:** QGIS does not support OAuth 2.0 for WFS at the time of writing. If you need to access restricted datasets you can use the WFS Proxy application detailed below.

#### Google Maps Engine Connector
Google has developed a Google Maps Engine Connector for QGIS 2.0+ that allows users to search for maps and layers, view layers, login to access restricted data, and upload vector and raster data.

[GME Connector installation and use instructions](https://docs.google.com/document/d/1b-FQS0O1q9y-RJxCk-oZTqbmryZSLYnago9lzCatjIY/edit?usp=sharing)

[GME Connector homepage](https://github.com/googlemaps/mapsengine-qgis-connector)

[Video: Google Maps Engine QGIS Connector is open source!](https://developers.google.com/live/shows/5452616121188352)

#### WMS & WMTS
QGIS natively supports public WMS and WMTS services without the need for any plugins. Since QGIS does not support OAuth 2.0 for WMS and WMTS you will need to use the Google Maps Engine Connector to access restricted map services via WMS.

### ArcGIS
#### WFS
ESRI does not yet provide WFS 2.0 support in ArcGIS Desktop. The best alternative solution for downloading vector features at this stage is to use FME 2014 and its Google Maps Engine integration features.

If you wish to add your voice to those asking for ArcGIS Desktop to support WFS 2.0 [vote on ESRI's offical ideas site](http://ideas.arcgis.com/ideaView?id=08730000000bvIKAAY).

> **Note:** The lack of support for WFS 2.0 in ArcGIS is one of the primary reasons Landgate is investigating a WFS 2.0 - 1.0 bridge.

#### Google Maps Engine Connector
Google has developed a Google Maps Engine Connector for ArcGIS Desktop 10.0+ that allows users to search for maps and layers, view layers, login to access restricted data, and upload vector and raster data.

[GME Connector installation and use instructions](https://drive.google.com/file/d/0B0kxJh5jFHnycGRuRnZLRHQ5d28/edit?usp=sharing)

[GME Connector homepage](https://github.com/googlemaps/mapsengine-arcgis-connector)

[Video: Google Maps Engine QGIS Connector is open source!](http://www.youtube.com/watch?v=in2IP4o79fQ)

#### WMS & WMTS
You should be able to continue using public WMS and WMTS services in ArcGIS as you have in the past. Since ArcGIS does not support OAuth 2.0 for WMS and WMTS you will need to use the Google Maps Engine Connector to access restricted map services via WMS.

> **Note:** ArcGIS 10.1 is required to utilise WMTS services.

### FME
FME 2014 comes with [Google Maps Engine integration](http://www.safe.com/highlight/google-maps-engine/) for both reading and writing data with Google Maps Engine. Safe Software also provides a separate (free) [FME Data Loader](http://www.safe.com/highlight/google-maps-engine/) for Google Maps Engine.


> @TODO Update and rewrite the QGIS WFS 2.0 plugin instructions
> @TODO WFS Proxy
