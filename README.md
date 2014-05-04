# MIDIExchange

[ ![Codeship Status for rkamradt/MIDIExchange](https://www.codeship.io/projects/1b298ee0-b566-0131-9539-2ea5d9165023/status?branch=master)](https://www.codeship.io/projects/20374)

A website that will allow users to exchange MIDI files

A detailed blog post covering this entire application can be found here:
http://rlkamradt.wordpress.com

 * Backbone.js
  * Handlebars
  * Browserify
  * Jasmine tests
  * Basic UI app
 * Express / Node.js
  * Handlebars
  * Mocha test runner
  * Chai, Sinon, Proxyquire tests
 * MongoDB
  * Mongoose
 * Bower
  * package.json
 * Grunt:
  * Bower install
  * Browserify
  * Handlebars (precompiled)
  * jsHinting
  * LESS
  * Minification/Uglification
  * Karma client testing/tdd
  * Mocha node testing
  * Watchers
  * Concatenation/Copy
  * Concurrent runs (server, karma, mongod, etc)

## Requirements

node 0.10+ (and npm), mongodb - visit nodejs.org and mongodb.com to download
each.

    $ sudo npm install -g grunt-cli
    $ npm install
    $ grunt init:dev

Grunt init:dev only needs to be run the first time to prepare the vendor.js
files.

## Running the App:

Start the server in DEV mode, with nodemon watching the app for a relaunch,
watchers on scripts and less files for rebuild.

    $ grunt server

Note: Windows users, for some reason the grunt shell task will not launch
mongod during runtime (so the node server will crash).  Be sure to launch
mongod in another window before starting grunt server.

### Front-end Tests/TDD:

Requires PhantomJS to be installed globally:

    $ sudo npm install -g phantomjs

To run tests in TDD watch mode:

    $ grunt tdd

To run tests once:

    $ grunt test:client

### Server Tests:

Server tests have been added using Mocha, Chai, and Proxyquire.  To run the
tests:

    $ grunt test:server

Note:

    $ grunt test

(will run all tests - both server and client)
