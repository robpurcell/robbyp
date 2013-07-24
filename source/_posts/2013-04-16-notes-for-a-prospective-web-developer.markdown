---
layout: post
title: "Notes for a prospective Web developer"
date: 2013-04-16  19:44
comments: true
categories: web
---
After a good while, my second blog posting, and the first of the new decade... Yes, at this rate my third will be in 2025!

Some notes on what I'm doing to get my my web application up and running.  Note, I'm running this effort in tandem with another blog post on using Vert.x, with the hope that these efforts may come together at some stage... We shall see.

####tl;dr I'm going to try and get a Bootstrap site laid out using Grunt and Compass.

### Install Grunt
```
npm install -g grunt-cli
npm install -g grunt-init
```
Get the gruntfile template, create Gruntfile.js and package.json
```
git clone git@github.com:gruntjs/grunt-init-gruntfile.git ~/.grunt-init/gruntfile
grunt-init gruntfile
npm init 
```
####Install grunt-contribs

Ensure that these are also referenced in Gruntfile.js!
```
npm install grunt-contrib-compass --save-dev
npm install grunt-contrib-concat --save-dev
npm install grunt-contrib-uglify --save-dev
npm install grunt-contrib-nodeunit --save-dev
npm install grunt-contrib-jshint --save-dev
npm install grunt-contrib-watch --save-dev
npm install grunt-contrib-qunit --save-dev
```

###Install Compass
Make sure Ruby is up to date, and Gems are on the PATH
```
ruby -v
brew upgrade ruby (if necessary)
export PATH=$PATH:/usr/local/opt/ruby/bin
```
####Create the SASS folder structure
```
compass create
```
####Add compass config to Gruntfile.js
``` javascript
grunt.initConfig({
  compass: {                  // Task
    dist: {                   // Target
      options: {              // Target options
        sassDir: 'sass',
        cssDir: 'stylesheets',
        environment: 'production'
      }
    },
    dev: {                    // Another target
      options: {
        sassDir: 'sass',
        cssDir: 'stylesheets'
      }
    }
  }
});
```
Make sure that config.rb and Gruntfile.js are consistent!
###Copy the Bootstrap files into place
Easy enough