---
layout: post
title: "Getting started with Vert.x"
date: 2013-07-23 07:16
comments: true
categories: web, vertx
---
Today, I'm trying to see if I can figure out what Vert.x is.  I'm following the installation doc [here](http://vertx.io/install.html).

I intalled Vert.x with [gvm](http://gvmtool.net/):

    $ gvm install vertx
    $ gvm current vertx
    Using vertx version 2.0.0-final


I created the Hello World example:

    $ vi server.js
    $ vertx run server.js
    Downloading io.vertx~lang-rhino~2.0.0-final. Please wait...
    Downloading 100%
    Module io.vertx~lang-rhino~2.0.0-final successfully installed


Then I started following the [Main Manual](http://vertx.io/manual.html)

Aside: running Vert.x on Heroku immediately jumped to mind: [found this](http://fbflex.wordpress.com/2012/05/02/running-vert-x-applications-on-heroku/)

Developing an app using Gradle for build management seemed like the way [forward](http://vertx.io/gradle_dev.html)

Clone template project locally:

    $ git clone https://github.com/vert-x/vertx-gradle-template.git my-vertx-module
    $ git remote rm origin
    $ git remote add --track master origin git@github.com:robpurcell/verdant.git
    $ git pull
    $ git push origin master

As per the above, I created the repo on Github and then merged in the cloned template: [see here](http://caiustheory.com/adding-a-remote-to-existing-git-repo) for some more details of the way to get remote tracking working properly.