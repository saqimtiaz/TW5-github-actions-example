# TW5-github-actions-example
**Example of how to use Github Actions to build and publish a TiddlyWiki**

Starting point: a wiki folder for TiddlyWiki on node.js, being saved to a Github repository.

In the root of your repository you need to:
* add a `package.json` file. You can do so via `npm` using `npm init`, or by copying and modifying the `package.json` in this repo.
* add TiddlyWiki as a dependency `npm install tiddlywiki`
* Add a script `build` by coping from the `package.json` in this repo and modify it so it corresponds to the command you would need to run in the root of your repository to build the TiddlyWiki. If your `tiddlywiki.info` file is in the repository root, you do not need to modify this.
  * You can verify that everything works so far by running the command `npm run build`, the wiki HTML file should be saved in the folder `output` in the root of your repository. This can safely be deleted after testing.
* In the root of your repository, copy the `.github` folder from this repository.
* Add these new files to Git, commit and push to Github.
* The TiddlyWiki will automatically be built and pushed to your `gh-pages` branch.
* If you do not already have Github Pages enabled for your repository, go to the settings page for your repository, choose Pages from the left hand menu. Under "Source" choose the branch "gh-pages" and save.
* Your wiki will be available at https://{username}.github.io/{reponame}, for example for this repo https://saqimtiaz.github.io/TW5-github-actions-example/