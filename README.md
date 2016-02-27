# [Measurement Lab](http://www.measurementlab.net/) Source Code

This is the source code of the Measurement Lab website built using [Jekyll](http://jekyllrb.com) and utilizing [GitHub Pages](https://pages.github.com/) to publish and host the site.

Current Build Status is: [![Build Status](https://secure.travis-ci.org/m-lab/m-lab.github.io.png?branch=master)](http://travis-ci.org/m-lab/m-lab.github.io)

## Local Development

**Please Note** This repository contains a submodule, so after cloning this repo, you will also need to run `git submodule init` and `git submodule update` to pull down the submodule files as well.

1. Install dependencies `bundle install`
2. Run Jekyll server to preview in development mode `jekyll serve`.
3. View the generated site by going to [http://localhost:4000/](http://localhost:4000/)

### HTML Compression

This site enables HTML Compression for optimizing performance.  If it is desired to not compress pages while doing development, developers can simply remove the ``layout: compress`` from the default template in the _layouts folder.  Please ensure to re-enable compression, however, before commiting code for review.

## Site Structure

| Directory | Description |
| ------------- |:------------- |
| _data | Directory contains yml files that contain content that is not within individual pages or posts. |
| _includes | Contains several partials that are common to several generated pages. |
| _layouts | Contains the templates that are used to generate the commonality of the pages (default is the main one that all the pages use. |
| _pages | Contains all non-blog post pages. Pages that have a number prepended to the filename signifies that they are used to dynamically generate the main navigational header.  They will display in the header in the order of the prepended numbers.  These pages also must contain the `menu-item: true` frontmatter in the pages. |
| _posts | Contains all of the individual blog entries. |
| css | Contains the css for the project. |
| fonts | Contains the customized font libraries for the project. |
| js | Contains the js libraries for the project. |
| images | Contains all the image files for the site |
| publications | Contains all the pdfs and docs that the site links too |

## Code Standards

This section highlights the coding standards to be used for this project to ensure consistency across the codebase for current and future development

### Filename conventions
- Should be all lowercase and words are concatenated with a hypen

### Variable naming conventions
- All yml frontmatter keys should be lowercase and words concatenated with a hyphen

### Liquid
- All liquid variables are following an underscore pattern so they can be easier to differentiate from yml frontmatter variables
- All liquid tags, objects, and filtesr will have spaces in front of and following whatever is contained within braces

