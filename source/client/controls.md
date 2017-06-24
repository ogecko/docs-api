title: Controls
description: Set of user interface components for controlling large document collections.
---

This module allows you to filter, sort, search and page through a large document collection. It provides methods to count the number of documents in the collection for pagination and filtering, with the ability to count categories and groups of documents as well. It also provides word vector indexing to allow quick searching of the results. 

The functionality relies on a definition of the fields that can be used for filtering and searching. The controls use the definition and modify the current FlowRouter URL so that it matches the current selections. There are methods to allow the URL to be converted into a MongoDB selector and modifier based on the URL parameters and query string. The selector and modifier can be used on the server for publishing a subset of the documents and on the client for visualising the subset of documents.

This module includes the following
- Template.SortBy
- Template.FilterBy
- Template.FilterText
- Template.Pagination
- Template.Search
- Select.defn
- Select.getScopeFromDefn
- Select.getSelectorFromParams
- Select.getModifierFromParams
- Select.expandLunr
- Counter.pages
- Counter.groups
- LunrIndex

