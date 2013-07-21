---
layout: post
title: "Playing with Vert.x"
date: 2013-04-16 08:09
comments: true
categories: web
---
Today, I'm trying to see if I can figure out what Vert.x is.  I'm following the tutorial here.

I intalled Vert.x with [gvm](http://gvmtool.net/):
```
$ gvm install vertx
$ gvm current vertx
```
####Using vertx version 1.3.1.final

First point to note: [Github](https://github.com/vert-x) has changed its url for module downloads, meaning you need to add a parameter to the command line: -repo vert-x.github.io.  I installed the required module manually:
```
$ vertx install vertx.web-server-v1.0 -repo vert-x.github.io
```
I also did this for the MongoDB persister (whatever that proves to be):
```
$ vertx install vertx.mongo-persistor-v1.2.1 -repo vert-x.github.io
```
I tried to discover how to update the deployModule command in the App.groovy file to take the new repo location, but I couldn't see where the configuration option (JSON) is documented.