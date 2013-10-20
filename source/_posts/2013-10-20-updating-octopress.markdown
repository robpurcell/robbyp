---
layout: post
title: "Updating Octopress"
date: 2013-10-20 22:21
comments: true
categories: [blog, octopress]
---
A few notes on updating Octopress; as always an aide-mémoire.

### Getting the blog onto Github
First things first, I finally got the blog tracked on Github.

    $ git remote rename origin octopress
    $ git remote add origin git@github.com:robpurcell/robbyp.git
    $ git config branch.master.remote origin
    $ git push -u origin master

That lot gets the origin (which was still pointing to the Octopress repo from the original clone) renamed to `octopress` and then a new origin created for my Github repo, freshly created.  Finally the content was pushed.

<!-- more -->
### Update the Octopress bits
Now tracking both my Github repos and the Octopress one, I can merge in the more recent changes since I created the site.

    $ git pull octopress master
    $ echo 1.9.3-p194 > .rbenv-version # The update had deleted this for some reason...
    $ rbenv rehash
    $ bundle install
    $ rake update_source
    $ rake update_style

The final two update scripts didn't seem to do too much, but I ran for completeness.
    