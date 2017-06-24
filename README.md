# Gehyra API Documentation

This is a [hexo](https://hexo.io) static site used to generate the [Gehyra API Docs](https://ogecko.github.io/docs-api).



## Generating the documentation
To generate the documentation use:
```
$ npm run gen
```
This script will 
1. Clean the Hexo database
2. Generate JSDoc `data/data.js` from the code signatures
3. Generate the static html pages from the markup. 

The generated files are stored in the `docs` folder. This folder is setup in GitHub to be hosted at [https://ogecko.github.io/docs-api](https://ogecko.github.io/docs-api). To redploy the site you will need to commit and push changes to this repository.



## Running locally
To run a copy of the documentation locally use:
```
$ npm run start
```
Changes to the markdown files will be automatically reflected. Changes to code signatures will need restarting of the server.



## Updating the theme

This repo links to the `docs-theme-ogecko` repository using submodules. To update to the latest theme use:

```
$ git submodule update --init
```
Generally you should not commit changes to the submodules, unless you know what you are doing.


