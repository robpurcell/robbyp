---
layout: post
title: "A quick aside on locale"
date: 2013-10-20 23:08
comments: true
categories: [blog, octopress]
---
While writing the previous blog post, I decided to use a nice `é` character.  Why not?  Well it turns out that the markdown/YAML parsing in Octopress doesn't like UTF-8 much.  The solution is in the [Internet](https://github.com/imathis/octopress/wiki/FAQ#using-non-ascii-characters-in-your-blog) although the answer there doesn't quite work.

With the help of [this blog](http://blog.remibergsma.com/2012/07/10/setting-locales-correctly-on-mac-osx-terminal-application/) I have nice non-ASCII characters in the blog now.  The link refers to the OS X Terminal app, but equally applies to iTerm2 that I use.

    $ locale
    LANG=
    LC_COLLATE="POSIX"
    LC_CTYPE="POSIX"
    LC_MESSAGES="POSIX"
    LC_MONETARY="POSIX"
    LC_NUMERIC="POSIX"
    LC_TIME="POSIX"
    LC_ALL="POSIX"
    $ export LANG=en_US.UTF-8
    $ export LC_ALL=$LANG
    $ locale
    LANG="en_US.UTF-8"
    LC_COLLATE="en_US.UTF-8"
    LC_CTYPE="en_US.UTF-8"
    LC_MESSAGES="en_US.UTF-8"
    LC_MONETARY="en_US.UTF-8"
    LC_NUMERIC="en_US.UTF-8"
    LC_TIME="en_US.UTF-8"
    LC_ALL="en_US.UTF-8"