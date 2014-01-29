# Welcome to SLIP Future

This is the technical documentation for SLIP Future (Shared Location Information Platform)$abbr$ $LINK$, the Western Australian Government's spatial data platform/service/repository/thingy.

SLIP Future is administered by Landgate and runs on Google's new cloud-based Google Maps Engine (GME) $LINK$ platform. Data are available as simple and easy GeoJSON via a RESTful API, via OGC services #LINK#, via simple out-of-the-box 2D and 3D viewers, and as a direct download.

Most of the data is made available under the WALIS... $info here about WALIS and CC licensing + a LINK$.

# Data, Please
## Locate
The *Locate* $LINK$ map service is the first publicly available in SLIP Future. It contains over $COUNT$ data layers from throughout the Western Australian Government from Landgate's latest aerial photography capture to public transport services to property information and much more.

More publicly available services will come on line as the SLIP Future project progresses, covering a broader range of datasets and including a range of paid subscription-only datasets. Throughout this documentation we will use the *Locate* service to demonstrate the capabilities of SLIP Future.

## Our Sandbox
@TODO Some words about the Sandbox and a way for people to apply for access. OR just a link to a separate Sandbox page with the info there.

## Google Maps Engine Primer
SLIP Future has partnered/is working with/something Google to deliver SLIP Future via their new Google Maps Engine platform. GME is based on the same technology that runs Google Maps and operates from Google's worldwide network of data centres to provide fast, scalable, and very reliable data services to the people of Western Australia.

You don't need to know (or care) a lot about GME and how it works under the hood except for this one key concept: GME operates on the basis of a datasource > layer > map hierachy where a datasource may be used to create multiple layers and a layer may be in multiple maps.

@TODO Do we need any overviewy stuff from Kylie's presentation?

## Less talk, more data!
Data in SLIP Future are available from a number of differing APIs each suited to their own particular type of reuse and data.

### The Google Maps Engine API
The GME API is a RESTful $LINK$ JSON-based API that understands SQL-like queries, is the recommended way to programmatically access data in SLIP Future, and provides three key areas of functionality:

1. Access to vector data sources (/tables/features $LINK$)
2. Data discovery (search and list maps, layers, and datasources) (/assets search $LINK$)
3. CRUD $LINK$ Create Replace Update Delete operations to create and modify datasources ($LINK)

#### Authentication
Most parts of the GME API require the use of a Google account and OAuth2 protocol. Google has excellent documentation, code samples, and libraries in a wide range of languages $LINK$ available at GME API Authentication and Authorisation ($LINK$ https://developers.google.com/maps-engine/documentation/oauth/).

The sole exception to this are public vector datasources, which can be accessed simply by provide an API key and making a request in your browser. For further instructions and working sample see Google's Accessing Public Data $LINK$ https://developers.google.com/maps-engine/documentation/public-read documentation.

### OGC Services


# Discovering Data


@TODO Link to WALIS Forum slides (mine) and the whole one (w/ D&K's)
@TODO Concepts
@TODO Getting Started

@TODO Something about search providing endpoints and shiny
@TODO Maps Engine API new features https://docs.google.com/file/d/0B0kxJh5jFHnydzhUZVVTTXpDb28/edit
@TODO GME limits. https://docs.google.com/spreadsheet/ccc?key=0AkkxJh5jFHnydEpxMTJEU2x2eldoVXpZb1EtSkJJVnc&usp=drive_web#gid=0 Link to proper Google doco?
@TODO A useful tutorial sandbox thing: https://developers.google.com/maps-engine/documentation/tutorial
@TODO At the end review http://management.apievangelist.com/building-blocks.html

My slides: https://docs.google.com/presentation/d/1d_ELFSY8Z7wFsoLP7At1AYEFczBg_q5vFt6HtgtczJs/edit#slide=id.g172161ce0_040
Merged WALIS Forum slides https://docs.google.com/presentation/d/1tuFn77lUE_9YO0DSOktZUqbuh6fktbkEoT0jo3ucdng/edit#slide=id.p17
New SLIP August 2013 slides https://docs.google.com/presentation/d/14rc1n99r1e3bkeRl9AkdKmee6lo5SlMeYLK1RTpq-To/edit#slide=id.p19

http://data.police.uk/
