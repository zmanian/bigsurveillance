This project uses grunt to minify JavaScript and LESS. It's based on the
[Composer.js](https://lyonbros.github.io/composer.js/) JavaScript MVC framework,
which is the best framework ever.

## Developing locally

* `npm install` to install packages,
* `grunt` to run grunt (automatically minifies JS and LESS)
* Host the project at `bigsurveillance.dev` to get TypeKit to work

## Code structure

**JavaScript:**

* `js/main.js` contains the main page logic. It uses AJAX to getthe user's
  location from [fftf-geocoder](https://fftf-geocoder.herokuapp.com) and also
  the Political Scoreboard spreadsheet from Google Docs. Once both of these are
  loaded, it spawns the Political Scoreboard Controller
* `js/compiled.js` and `js/compiled.min.js` are automatically compiled by Grunt.
  You shouldn't edit these directly.
* `js/controllers`: contains all Composer controllers
* `js/models`: contains all Composer models and collections
* `js/views`: contains all Composer views. Right now we're just using raw
  JavaScript to create DOM elements for the views. It's not pretty, but it's
  really fast.

**CSS / LESS:**

* `css/core.less`: The LESS source for the project
* `css/core.min.css`: Minified CSS compiled by Grunt. Don't edit this directly.