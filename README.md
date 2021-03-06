# KitchenSink Boilerplate

Use all the JS goodies!
 * Express
 * Grunt
 * Bower
 * Handlebars client/server
 * Knex migrations
 * Bookshelf.js ORM
 * Passport.js Auth
 * Browserify
 * LESS + Autoprefixer
 * UglifyJS, CSSmin, imagemin
 * Mocha with Chai assertions
 * QUnit via PhantomJS
 * JShint + HTMLtidy
 * LiveReload for all the above


Bundled client-side libs:
 * jQuery
 * Normalize + Pure CSS
 * Backbone.js
 * Font-Awesome


### dependencies

`brew install node mysql`

`npm install -g grunt-cli bower`

`cd kitchensink-boilerplate && npm install`

### create database

`mysql.server start && mysql -uroot -e "CREATE DATABASE kitchensink"`

There is no login, but there are tests for the stub User model.

## Usage

 * `./etc` contains configuration. files that match `/etc/*secret*` are git-ignored 
 * `./app/client/*.js` is _browserified_ on save when using `grunt dev`
 * `./app/client/css/*.less` is also compiled and fed through _autoprefixer_ on save.
 * `./app/server/templates` contains the server-side views, layouts & partials.
 * `./app/server/controllers` is where you would add routes. you can override what css/js to include for a given route by modifying `res.locals.page`

### build it

`grunt build:prod` will generate all assets including minified versions.

### pass the tests

`grunt test` and `npm test` do the same thing: run all tests.

`grunt qunit` builds and runs the client-side tests only.

### run the server

`grunt dev` for the live reload magic.

`npm start` to run in the background, `npm stop` to cancel.

`NODE_ENV=production node server.js --server.port=3001 --sessions.secret=foo` run in production mode, eg to try minified assets



