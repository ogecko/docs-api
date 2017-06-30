# docs-theme-ogecko
A pure, simple and responsive Hexo theme for documenting technical information eg architecture, design, api, and process. Inspired by the [Meteor Guide](https://guide.meteor.com/) and [API Docs](http://docs.meteor.com/).

Includes support for the following features
* Navigation autogen sidebar and menu
* Code Signatures using JSdoc and apibox
* Google analytics and Segment Tracking
* Search and Indexing using Lunr and Algolia 
* Website Notification via Twitter using Nectar Ninja

## Adding this Theme to a Hexo site
1. Add this respository as a submodule to your site.

```
$ git submodule add  https://github.com/ogecko/docs-theme-ogecko/ yourproject/themes/ogecko
```

2. Edit the `_config.yml` file and change the following

```
theme: ogecko
api_box:
  data_file: 'data/data.js'
```


## Known **oGecko** repos that this theme is used by:
* https://github.com/ogecko/docs-api/
* https://github.com/ogecko/docs-kb/
* https://github.com/ogecko/docs-process/

If a change to this theme is made, those repos need their Git submodules updated.

## Semantic UI Themes
Semantic UI provides a lot of flexibility in theming and componentisation. This Hexo theme includes the full semantic-ui package and allows regeneration of the `semantic.min.js` and `semantic.min.css`. As such this theme can be tailored in many ways.

To regenerate the distribution files `semantic.min.js` and `semantic.min.css`.
* Run the command
``` 
$ npm run semantic 
```

To modify which elements, collections, views, or modules are included in the distribution files. 
* Edit `semantic.json` and add additional items to the `components` field.
* A full list of components are available in the [Semantic Docs](https://semantic-ui.com/introduction/build-tools.html#semanticjson).

To choose which packaged theme to use on a per component level .
* Edit `src/theme.config` and set the theme for each component.
* A list of available packaged themes per component is listed under the `n Themes` Button at the top of each component definition page in the [Semantic Docs](https://semantic-ui.com/elements/button.html). 

To tailor global variables for the site. eg the color scheme
* Edit `src/site/globals/site.variables` and modify the sitewide defaults.
* A list of variables can be found at `src/themes/default/globals/site.variables`.

To tailor individual components from the packaged theme. eg making checkboxes use your primary color. Note that component variables are typically based on the global variables but are more specific to the component.
* Edit the individual components variables. eg `site/modules/checkbox.variables`.
* A list of variables can be found at `src/themes/default/elements/site.variables`.

To add additional CSS rules to a definition of a component or globally.
* Edit `src/site/(collections|elements|modules|views|globals)/(filename).overrides`

