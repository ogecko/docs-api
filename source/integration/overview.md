title: Overview
description: High Level Domain Integration using Job Collections and Adapters
---

The intent is to push integration requests to the highest level of understanding as possible. Each application domain will have their own topics of requeusts that need to be able to be handled by the set of domain specific adapters. Your application and the adapters are totally free to chose topics, requests and interactions to best get the job done.

Some adapters are static and simply push events and metrics into Gehyra on a regular basis. Others are more dynamic and respond to the needs of the application in real time. Most applications will at least need some form of searching, fetching and interacting with an integrated device or service. This overview describes how the work pipeline manages and processes these types of requests.

<h2 id="pipeline">Searching, Fetching and Interacting</h2>

Action dispatchers create a work job that is queued into a [Job Collection](https://github.com/vsivsi/meteor-job-collection). You can dispatch a `SearchJob` that will use all registered search services on a given topic to get a list of results to fetch. You can dispatch or schedule a `FetchJob` to retrieve some content then parse and store its information. You can dispatch an `InteractJob` to perform some task by interacting with a network service. 
- dispatchSearch :: Topic, Params -> SearchJob
- dispatchFetch :: URL -> FetchJob
- dispatchInteract :: URL -> InteractJob
- scheduleFetch :: URL, Schedule -> FetchJob

Workers monitor the [Job Collection](https://github.com/vsivsi/meteor-job-collection) and then process each particular type of job. They are responsible for updating progress on the job and correctly reporting back any errors on the job.
- processSearchJob :: SearchJob -> FetchJobs
- processFetchJob :: FetchJob -> Knowledge, [FetchJobs]
- processInteractJob :: InteractJob -> Knowledge

<h2 id="adapters">Domain Specific Adapters</h2>

The requesting, fetching, parsing and storing of information is typically domain specific. An `Adapter` is used to define how to perform these activities for a given domain and URL template. When registering an `Adapter` the functions to perform these activities are defined.
- registerAdapter ::

<h2 id="fetching">Searching and Fetching Content</h2>

When processing a `SearchJob`.
- findUrls :: Topic, Params -> URLs

When processing a `FetchJob`.
- findAdapter :: URL -> Adapter
- setupRequest :: URL -> Request
- fetchRequest :: Request -> Content
- parseContent :: Content -> Information
- storeInformation :: Infomation -> Collection | FileCollection

When fetching a `Request`.
- readFromCache ::
- readFromNetwork ::
- readFromBrowser ::

<h2 id="parsing">Parsing information out of Content</h2>

When parsing `Content`.
- parseHTML ::
- parseCSV ::
- parseCSVMarkup ::
- domCheck ::
- domSelect ::

When parsing `HTML` elements.
- isHTML ::
- combine ::
- parseRegex ::
- getFieldType ::
- getSelectedHtmlElements ::
- getValuesOfElements ::


<h2 id="learning">Learning from the parsed content</h2>

When learning using `Natuaral Language`.
- defineKnowledge ::
- normalizeString ::
- compactArray ::
- compactFlatArray ::

- extractIdeas ::
- extractSentances ::
- extractTerms ::
- extractNgrams ::

- refineIdeas ::
- chooseAll ::
- chooseAllWithout ::
- chooseLast ::

When storing `Information` for later recall.
- storeContent :: Content -> Collection Knowledge
- storeData :: Data -> Collection Knowledge
- storeFile :: URL -> FileCollection Knowledge

<h2 id="interacting">Interacting with network services</h2>

When processing an `InteractJob`.
- interactWithBrowser ::
- storeInformation :: Infomation -> Collection | FileCollection



