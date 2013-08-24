---
layout: post
title: "A Note About Git"
date: 2013-08-24 13:00
comments: true
categories: [git, python]
---
A colleague mentioned the [Python Koans](https://github.com/gregmalcolm/python_koans) as a nice set of exercises to do in a spare moment.  I cloned the repo and started having a go.  Then I realised that I should have forked the repo so I could share my progress ;-)  Here's the steps:

    -- Fork on github.com
    -- Clone using Github for Mac
    cd python_koans
    git remote add upstream https://github.com/gregmalcolm/python_koans.git

From my original clone:

    git add .
    git commit -m 'The files I changed'
    git format-patch origin/master --stdout > my.patch

And then back to my new forked repository:

    git apply my.patch
    git add .
    git commit -m 'The files I changed'
    git push origin master

Ta da!