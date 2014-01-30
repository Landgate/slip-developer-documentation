# Register
Registering to access data in SLIP Future is as simple as using your existing Google account or creating a new account at [Google Account Signup](http://accounts.google.com). If you have an existing email address (i.e. a work email, or another email provider) you can simply create a new account linked to that email as well.

Once you have your Google account setup and you're logged in you'll be able to:

* Create API keys to access public data on the [Google Developers Console](https://cloud.google.com/console/project)
* Create OAuth2 clients to use the full capabilities of the GME API and any private data you have been granted access to
* Login to the Google Maps Engine console and adminster your maps and data services (Editors Only)

# Authenticate
Authentication in SLIP Future comes in two flavours: Google API keys and OAuth 2.0 and is required for any application using the [GME API](https://developers.google.com/maps-engine/) or WFS.

You DO NOT need to authenticate to access public data via WMS, WMTS, or the Google Maps JavaScript API. 

## OAuth 2.0
If you're not familiar with the OAuth 2.0 protocol there are a few good resources [here](http://blog.varonis.com/introduction-to-oauth/) and [here](http://oauth.net/about/). In essence it boils down to clients and servers exchanging a set of private details identifying the client in return for time limited access tokens. Unlike older authentication approaches like HTTP Basic there is no need for clients to exchange sensitive information such as passwords.

Google has produced a great and easy to follow set of documentation on [getting staretd with OAuth 2.0 for Google Maps Engine](https://developers.google.com/maps-engine/documentation/oauth/). There you'll find an explanation of:

* Explanation of each OAuth flow (basically, your type of application - client-side, web backend, installed, server-to-server)
* Code samples for each flow
* Links to the client libraries Google has made available for working with OAuth

## API Keys
When accesing public vector data in SLIP Future it is possible to use Google API keys instead of the more complicated OAuth 2.0 protocol. API keys are created in the Google Developers Console and simply included in the URL for any call to access vector data via the GME API.

See Google's [Accessing public data](https://developers.google.com/maps-engine/documentation/public-read) documentation for more information and an example of how to start retrieving data.

## Google Developers Console
Regardless of the type of authentication you are applying you'll need to create a new project in the [Google Developers Console](https://cloud.google.com/console/project) to be able to access the GME API.

1. Go to the [Google Developers Console](https://cloud.google.com/console/project) and *Create a new project*. It doesn't matter what you call your project, but something memorable like "SLIP Future {Application}" would probably be good.
2. Go to the *APIs & auth* section
3. Ensure that the *Google Maps Engine API* is set to *ON*
4. Choose the *Credentials* link
5. At this point you will need to choose whether to create an *OAuth client* or a *Public API access* client.

# Documentation

# Error Codes

# Code Samples

# Halp!

Keep it simple, only provide what's needed to just get started.

You know, the actual *Locate* data that they can use now. AssetIds and shit.
