---
layout: post
title: "Ratpack and Lazybones"
date: 2013-08-04 15:26
comments: true
categories: 
---
So [previously](/blog/2013/07/23/playing-with-vertx/) I started trying to figure out VertX.  While I still like the idea of that, I've detoured into looking at [Ratpack](http://www.ratpack-framework.org) as it appeals to the old Grails hand in me.  While I'm fond of Grails, and looking forward to seeing where it goes, I can't help but feel that the lightweight approach is what I need to start our in my adventure of building a HTML 5 app with AngularJS and Bootstrap.  See [here](/blog/2013/04/16/notes-for-a-prospective-web-developer/) for my tentative first steps with the client-side.  Hopefully this will all come together.

Used [Lazybones](https://github.com/pledbrook/lazybones) to create a template project, having setup the Github [repo](https://github.com/robpurcell/grat)

    lazybones create ratpack .

It sets up a nice, basic project layout.

I needed to add the IDEA plugin to `build.gradle`

    apply plugin: 'idea'
    ./gradlew idea

Next up... installing Bootstrap and AngularJS!
