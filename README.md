# Inclusion. Sass / Scss / Stylus Framework

##Contents
* [About](#about)
* [How to start](#how-to-start)
    - [Structure](#structure)
    - [HTML and CSS naming](#html-and-css-naming)
    - [Dependencies](#dependencies)
* [Live examples](#live-examples)
* [TODO](#todo)
* [Changelog](#changelog)
* [Credits](#credits)
* [License](#license)

## About
Inclusion is lightweight preprocessor single-page framework with next features:

* Simple and minimalist design
* Responsive layout
* Light and dark color schemes
* Clean typography
* Ready-to-use common elements 
* DRY output css code

And extra options:

* Extra positioned elements
* Grid mixin for custom grids
* Custom color schemes
* jQuery lazy image loading and image preview

![Mockup demo](pic.jpg)

## How To Start
Want to learn more about Inclusion, see demo or start using it? - Follow this: [Demo](http://orlovmax.com/lab/tools/inclusion) and [Tutorial](http://orlovmax.com/lab/tools/inclusion_dark-side).
For further development you should use grunt and bower, see more details about grunt installation [here](https://github.com/orlovmax/front-end-scaffold#how-to-start) and about bower [here](https://github.com/orlovmax/front-end-scaffold#bower)

To compile this project, please run the following:

* `npm install` - install grunt packages
* `bower install` - install dependencies
    - `grunt bower-dev` - compile dependencies and remove bower_components folder
* `grunt` - default task, compile project files

To create build version, please run build task:
* `grunt build`

##Structure
This project based on [frontend-scaffold](https://github.com/orlovmax/front-end-scaffold):

`/dev/` folder - contains source code.

`/build/` folder - build version, in our case - demo.

UPDATE: `/styles/` folder in `/dev/` contain two version of framework - extend and mixin. Also there are Scss and Sass versions.

- `Extend` version based on placeholders which make code more dry but if we have a lot of similar elements code will become messy. This version really cool for projects that have custom markup classnames with the same styles.
- `Mixin` version based on mixins so compiled code is more pretty and readable but there are duplication of mixin content for each element. In result we have a bigger stylesheet. This version works fine for small projects. Must say, that stylesheet size at all isn't so critical for common project that has built with `mixin` version.

### HTML and CSS naming

For this project I've used BEM naming: `.block` for independent block. `.block__element` for elements inside this block. And `.block_modifier` for modification of this block.

States of the form error messages use prefix `.is-*`. For example `.is-closed` - means closed nav or spoiler, `.is-opened` - open navbar and changed.

Js hooks use prefix `.js-*`.

###Dependencies
Inclusion plugins require jQuery library. So this dependency was included into `bower.json` for the further development.

## Live examples
* [Inclusion jekyll theme for my blog](https://github.com/website-templates/jekyll-inclusion)
* [Miniature wookie](http://orlovmax.com/lab/tools/miniature-wookie)
* [Simple contact form](http://orlovmax.com/lab/simple-contact-form)
* [Browser update screen](http://orlovmax.com/lab/browser-update-screen)
* [Pixel perfect tool](http://orlovmax.com/lab/tools/pixel-perfect-dev)
* [Vertical timeline](http://orlovmax.com/lab/vertical-responsive-timeline)
* [Inclusion: dark side](http://orlovmax.com/lab/tools/inclusion_dark-side)
* [Inclusion](http://orlovmax.com/lab/tools/inclusion)

## TODO
* Shortkeys list for snippets. Make snippet completion or something like that.
* Stylus version
* No-preprocessor version

Please note, that custom fonts, like Open Sans and Open Sans Condensed linked to the framework using @import directive. For better performance please use `<link>` tag in your markup `link(href='http://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,800italic,300,400,600,700,800|Open+Sans+Condensed:300&subset=latin,cyrillic', rel='stylesheet', type='text/css')` or local copies of these fonts

## Changelog
* v2.3 (July 19, 2015)
  - Autoprefixer instead of _elements lib
* v2.2 (January 06, 2015)
  - Sass version
* v2.1 (December 22, 2014)
  - Added IE8 support
* v2.0 (December 18, 2014)
  - Added mixin version of framework
* v1.5 (December 16, 2014)
  - Added video option for figure element
* v1.4 (November 24, 2014)
  - Added $color option for sections
* v1.3 (November 20, 2014)
  - Standalone anchor scrolling script added
* v1.2 (November 08, 2014)
  - Sublime snippets added, selection mixin added
* v1.1 (November 04, 2014)
  - Stable version
* v1.0 (August --, 2014)
  - Initial commit

## Credits
* [Lazy load plugin](http://www.appelsiini.net/projects/lazyload)
* [Intense Image Viewer](http://tholman.com/intense-images/)
* [Prism syntax highlighter](http://prismjs.com/download.html)
* [Detect Mobile Browsers](http://detectmobilebrowsers.com/)
* Product mockup created with [http://frame.lab25.co.uk/](http://frame.lab25.co.uk/)

## License
[MIT](http://opensource.org/licenses/MIT)