# Mike Ball

http://github.com/mdb/wp2middleman

# wp2middleman overview

* What is it?
* What's middleman?
* Basic demo
* My pitch
* Next steps

# What is wp2middleman?

A commandline tool that migrates Wordpress posts to Middleman-style markdown files.

# Its name

"wp2middleman" ?

Dude, its name is kinda goofy.

# What's Middleman?

http://middlemanapp.com

# Middleman workflow

Work locally and compile source code to a directory of HTML, CSS, and JS flatfiles.

* asset pipeline
* sensible layout system
* integrates nicely with template languages
* nice extension ecosystem
* data/content lives in markdown files

# 2014-01-14-hello-world.html.markdown

```
---
title: Hello World
date: 2014-01-14
tags: foo, bar, cats
---

A paragraph of content.
```

# Why a static site?

Less is more.

* no DB
* no application server
* no moving parts
* no cry

# Why did I create wp2middleman?

tl;dr

I needed it; it didn't already exist (surprisingly).

# How's it work?

```
wp2mm some_wordpress_export.xml
```

# Demo Time!

wordpress site: localhost:8888/wp2mm_demo
middleman site: localhost:4567

# My pitch

Get involved and help me make it better.

* simple tool; clear use case & need
* beginner & intermediate friendly
* could be a solid Philly contribution to the larger Ruby community

# What's next?

Make it better.

* growing feature list; getting some attention
* use it and file bugs
* plenty of room for improvements
* an online migrator?

# Thanks

https://github.com/bensheldon
https://github.com/monfresh

# Questions?
