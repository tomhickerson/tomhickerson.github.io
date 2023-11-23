---
title: "Working with Github Pages"
date: 2023-11-19T17:38:47+02:00
draft: false
toc: false
featuredImg: https://live.staticflickr.com/65535/53340238394_6f4c50b9d2_b.jpg
images:
ShowLastmod: true
Lastmod: 2023-11-23T19:38:47+02:00
tags: 
  - git
  - blog
  - working
---
I'm starting to work on this blog again to get away from the WordPress way of working with things, that is, to have someone else set up the MySQL and PHP and hope it's all the right version, and hope that updates don't break modules, and hope that a PHP upgrade doesn't cost extra in hosting support fees, and hope that... well, you get the idea.

I originally started with [a short article](https://chrisjhart.com/Creating-A-Simple-Free-Blog-Hugo/) about deploying to Github with Hugo, however a few things had changed since then:
- Hugo itself now uses a '''hugo.toml''' file instead of '''config.toml'''
- Github now offers a one-click support for Hugo actions, so there's no need to roll your own Action '''.yaml''' file

Also it's worth it to research your theme locally for a while, before pushing anything to Github.  I rushed that a bit and had to change themes mid-stream, but am now getting it all working. 

Working with Github Pages has also helped me understand Git a little more, like using things like [git rm](https://www.atlassian.com/git/tutorials/undoing-changes/git-rm) and [git submodule](https://www.atlassian.com/git/tutorials/git-submodule). 
