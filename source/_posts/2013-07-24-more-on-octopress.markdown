---
layout: post
title: "More on Octopress"
date: 2013-07-24 08:11
comments: true
categories: blog, octopress
---
I've been blogging with Octopress for a few days now.  The first good sign is that I am actually still doing it after a few days, thus breaking my usual install-fiddle-and-forget cycle.  Here are some notes I made while installed it onto my MacBook Pro.

### tl;dr Install Octopress and deploy to Heroku

#### Installing Ruby
You need to ensure that the correct version of Ruby is installed.  The approach [here](http://octopress.org/docs/setup/rbenv/) works.
    $ rbenv install 1.9.3-p194 # seems like the version Octopress wants in the .rbenv-version file
    $ rbenv rehash

#### Octopress source installation
You clone the Octopress git repository, and then configure it how you like it.  Very straightforward to get the [source](http://octopress.org/docs/setup/).
    $ git clone git://github.com/imathis/octopress.git robbyp
    $ cd robbyp/
    $ ruby --version
    $ gem install bundler
    $ rbenv rehash
    $ bundle install

#### Moving onto deployment
Gonna try out [Heroku](http://octopress.org/docs/deploying/heroku/)! 
Installed the [Heroku Toolbelt](https://toolbelt.heroku.com), as it seems the preferred approach now.  Octopress install guide is out of date with regard to this.
    $ heroku apps:create robbyp
    $ vi .gitignore # remove the public entry
Made sure the Heroku version of Ruby is consistent by adding `ruby "1.9.3"` into `Gemfile` in the root folder.

#### General workflow
Now that I'm setup, the workflow is something like:
    $ rake new_post["More on Octopress"]
    $ vi source/_posts/2013-07-24-more-on-octopress.markdown # oh yeah!
    $ rake generate
    $ rake preview
    $ git add .
    $ git commit -m '<Message>'
    $ git push heroku master    

The blog posts are written in [Markdown](http://daringfireball.net/projects/markdown/syntax#link), which is nice.

#### Wanted Twitter integration
Seems it was switched off in Octopress recently.  Searched around a bit and found [this](http://blog.jmac.org/blog/2013/03/30/putting-twitter-back-into-octopress/).

#### Get the domain alias working
    $ heroku domains:add www.robbyp.com
And a few bits of config at [joker](http://joker.com)