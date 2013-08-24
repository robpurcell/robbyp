---
layout: post
title: "Vert.x with a Gradle build"
date: 2013-07-24 18:34
comments: true
categories: [vertx, web]
---

I [previously](/blog/2013/07/23/playing-with-vertx/) set up Vert.x with a Gradle build.  Now it's time to have a play with it and see what we can do.

    $ ./gradlew test

A lot of stuff downloads!

    ./gradlew idea

To install the support for IntelliJ.

Moving on to the [dev guide](http://vertx.io/dev_guide.html).

Downloaded the [examples](http://vertx.io/examples.html).  Running the Groovy webapp:

    cd vertx-examples/src/modules/groovy/webapp
    vertx runmod io.vertx~example-web-app~1.0

As `webapp` has a `mods` folder, the vertx command can discover the module and run it.  See [here](http://vertx.io/mods_manual.html#how-vertx-locates-modules) for details.

