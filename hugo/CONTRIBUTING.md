# Contributing to Hugo Docs
### Before you start
Before you begin, get familiar with [Hugo](https://gohugo.io/). 

The Hugo docs use a theme called Clyde, which you can learn about [here](https://gewenyu99.github.io/clyde-example-app/). 

Once you have Hugo installed on your local machine, you can proceed.

### Running Hugo docs locally
Running `make run` in the root directory of `ga4gh-search` will start a development server. You can access it at: `http://localhost:1313/ga4gh-search/`. 

Most changes will reflect in real time via hot reload, structure changes to layout will require a recompile. **Make sure you disable caching in your browser!**

To test compile, run `make build`, this will compile into a git ignored folder.

To build for prod, we have a command called `make build_prod`. **DO NOT RUN THIS** during development, this is left for Travis, as the artifacts go to a folder that is tracked, so Github pages can get the compiled artifacts from the gh-pages branch.