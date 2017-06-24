# Gehyra API Documentation - https://ogecko.github.io/docs-api

This is a [hexo](https://hexo.io) static site used to generate the [Gehyra API Docs](https://ogecko.github.io/docs-api).



## Generating the documentation
To generate the documentation use:
```
$ npm run gen
```
This will clean the Hexo database, generate JSDoc `data/data.js` from the code signatures, then generate the static html pages from the markup. The generated files are stored in the `docs` folder. This folder is setup in GitHub to be hosted at [https://ogecko.github.io/docs-api](https://ogecko.github.io/docs-api).



## Running locally
To run a copy of the documentation locally use:
```
$ npm run start
```
Changes to the markdown files will be automatically reflected. Changes to code signatures will need restarting of the server.



#### Submodules

This repo links to the docs-theme-ogecko repository using submodules. To update to the latest theme use:

```
$ git submodule update --init
```
Generally you should not commit changes to the submodules, unless you know what you are doing.



#### Generating `data.js`

To generate the api boxes, the site uses a file `data/data.js` which is generated from the js docs. This will automatically happen whenever you start your local hexo server.

#### Starting hexo

Ensure you've run `npm install`. Then simply `npm start`.
