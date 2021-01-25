# Contributing to Hugo Docs
### Before you start
Before you begin, get familiar with [Hugo](https://gohugo.io/). 

The Hugo docs use a theme called Clyde, which you can learn about [here](https://gewenyu99.github.io/clyde-example-app/). I suggest referring to this to figure out how to edit layout, configurations, theming, etc.

Once you have Hugo installed on your local machine, you can proceed.

### Running Hugo docs locally
Running `make run` in the root directory of `ga4gh-search` will start a development server. You can access it at: `http://localhost:1313/ga4gh-search/`. 

Most changes will reflect in real time via hot reload, structure changes to layout will require a recompile. **Make sure you disable caching in your browser!**

To test compile, run `make build`, this will compile into a git ignored folder.

To build for prod, we have a command called `make build_prod`. **DO NOT RUN THIS** during development, this is left for Travis, as the artifacts go to a folder that is tracked, so Github pages can get the compiled artifacts from the gh-pages branch.

### Folder Structure
`ga4gh-search/hugo/content/docs`: You can find the main content of the docs here.

`ga4gh-search/hugo/content/api`: Redoc docs (OpenAPI 3 specs) are compiled to this folder from `ga4gh-search/spec/search-api.yaml`. See `build_api_docs` from the Makefile.

### Updating Clyde
Clyde is a git submodule. The submodule points to a tagged branch, if there is a new tagged branch to point to, first `cd` to the `ga4gh-search/hugo/themes/clyde` folder and fetch/pull the new tagged branch.

The main repository(ga4gh-search) refers to a commit of the nested submodule repository, which means you'll need to commit the changes in the main repository after updating/pulling the submodule.