# Tips & Tricks
## GME API
1. Can I choose which attributes to return from calls to the GME API?

> Yes! There's a little hidden feature in the form of the `fields` parameter that allows you to choose the attributes you want returned. It also works for any call to the GME API, not just `/tables/features`!
>
> e.g. `fields=assets/id,assets/name,nextPageToken` would return only the id and name attributes and the nextPageToken field.


# FAQs

## GME API & WFS
1. Where's the *LIKE* operator? How do I retrieve features and filter by part of a string?
> There is currently no support for LIKE in the GME API or WFS. Google have added this to their roadmap for us and we'll update you when we have an ETA.

2. I'm trying to do find all of the features intersecting a polygon and I'm just getting an error.
> Polygon vertices must be specified in counter clockwise order and must close the polygon (i.e. the first and last vertices must be the same). Check out Google's [*intersects* documentation](https://developers.google.com/maps-engine/documentation/read#geographic_restrictions).

3. I keep getting an *"Insufficient permissions for this action"* error
> If you're sure you have access to the layer check that you have specified `version=published` (GME API) or `assetVersion=published` in your request.

4. I can't query and filter by string attributes? $LINK$ insert error
> You've probably either fogotten to quote the attribute names in your request. Also remember that you need to urlencode your `where` parameter. Check out Google's [GME API queries](https://developers.google.com/maps-engine/documentation/read#queries) documentation.

5. I keep getting rate limit errors!
> The GME API defaults to a rate of 1 query/second and allows up to 300 queries/second for requests to `/tables/features`. If you're making multiple subsequent requests you'll need to force your application to sleep between requests to keep within these limits. For further information on limits see the [GME rate limits](https://developers.google.com/maps-engine/documentation/limits) documentation.

6. I get a $LINK insert error message saying the vector table is too big
> By default unverified clients are restricted to querying small vector tables and at a reduced rate of queries/second. If you require access to large vector tables please contact us, providing your Google Developer Console ClientID and we'll be happy to have your account verified for the higher limits.
