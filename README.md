Web Application Guidelines 3.0
==============================

**This version is deprecated**, see https://malmo.se/wag for the latest version.

Guidelines for The City of Malmö’s intranet applications.

## Editing the Guidelines
This repository contains the source for the guidelines. Content is written in markdown using the [kramdown](http://kramdown.rubyforge.org/syntax.html) dialect and the pages are found in the `pages` directory in the `gh-pages branch`.

## Publishing
The guidelines are published as [Github pages](https://pages.github.com/) using [Jekyll](https://jekyllrb.com/). Publishing of the content is triggered when the gh-pages branch is updated. This happens when you push to that branch or if you edit a page directly on Github (the latter forces a push).

## Developing
Checkout the gh-pages branch. Install Jekyll if you haven't done it before:

``` shell
$ gem install jekyll
```

Run Jeykyll and tell it to generate pages when they are changed:

``` shell
$ jekyll serve --baseurl "" --watch
```
Go to [http://localhost:4000/](http://localhost:4000/)


## Editing Sass and Coffeescript
There are a few asset files in the gh-pages branch used for the WAG itself. The source is available in the `stylesheets` and `javascripts` directories. To compile during editing, start one or both of the following watchers:

``` shell
$ sass --watch stylesheets/application.scss
$ coffee -c -w javascripts/application.coffee
```

You must compress the assets before pushing to Github if you edited them. This is not necessary if you just edit page content. Run the build script:
``` shell
$ ./build.sh
```

Now you are ready to commit and push to Github.


## License
Released under AGPL version 3.
