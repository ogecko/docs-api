title: Fetching
description: Fetching a HTTP request from Cache, Network or Broswer 
---

When processing a `FetchJob`.
- findAdapter :: URL -> Adapter
- setupRequest :: URL -> Request
- fetchRequest :: Request -> Content
- parseContent :: Content -> Information
- storeInformation :: Infomation -> Collection | FileCollection

When processing an `InteractJob`.
- interactWithBrowser ::
- storeInformation :: Infomation -> Collection | FileCollection

When fetching a `Request`.
- readFromCache ::
- readFromNetwork ::
- readFromBrowser ::


This module provides a managed approach to fetching HTML content from over the network, implementing the following three best practices
1. Minimal Impact – Dont spam servers asking for the same content. Cache all requests.
2. Minimal Latency - Wherever possible use a single HTTP request for the content.
3. Dynamic Content - Cater for pages that generate content using client-side Javascript. 

When an URL is requested the module will check whether there is a copy of it stored in the MongoDB cache. When there is a copy in cache which is not stale then it will return this instead of going out over the network. 

{% apibox fetchUrl.readFromCache %}

Read the URL using direct HTTP network requests.

{% apibox fetchUrl.readFromNetwork %}


Read the URL using a browser to callup the page and allow javascript to fully render any dynamic content.

{% apibox fetchUrl.readFromBrowser %}





