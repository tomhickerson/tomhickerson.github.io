---
title: "Seven Things I've Learned About Working With Hugo and Github Pages"
date: 2024-01-31T12:27:49+02:00
draft: false
toc: false
images:
featuredImg: https://live.staticflickr.com/65535/53340355026_56dcac41ac_h.jpg
tags: 
  - git
  - hugo
  - working
---
Since I've set this site up three months ago, I have worked with two other sites to get going on Github Pages and Hugo.  I've collected some impressions here, so that others working on the same setup can learn from my mistakes.

In general, I sought out Hugo as the lightweight Wordpress alternative - I would have WP on another hosting service, and all of a sudden get dinged for an extra charge if the latest version of PHP didn't work with the plugins I had installed, which I found very very annoying.  So I started moving away from WP and getting into static site generators a while back, and found that Hugo was the easiest to install and work with.

That having been said, there are a few tripwires you need to be mindful about when you start working with it.  Namely, the following:

1. When you pick a theme, make sure you are confident in the documentation.  Namely, make sure you understand how to add new content, and how to update the style to match your own personal taste.  If you're not 100% confident in your theme's documentation, move on quickly.
2. Hugo by default won't let you use most markup in the markdown - [this can be remedied in your config file if you want](https://gohugo.io/getting-started/configuration-markup/) - but instead you should lean into the [shortcodes](https://gohugo.io/content-management/shortcodes/) that it does provide.
3. Besides shortcodes, you should keep [the markdown guide handy](https://www.markdownguide.org/basic-syntax/#headings), just in case.
4. When you start to work with Github pages, keep in mind that a previous post I linked to a reference that prompted you to roll-your-own Github Action.  That is no longer necessary, as you can just go to Settings > Pages and then select 'Github Actions' under 'Build and deployment'.  The 'Hugo' action works very well out of the box, which was a nice surprise.
5. That having been said, if you are setting up a custom domain, make sure you read and then re-read [the docs thoroughly](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site#configuring-an-apex-domain).  Setting up the apex domain is straightforward, but you may need a few trys to get the 'www' URL to work for you.
6. Never use ```git clone``` to download your themes, always use ```git submodule```.  This means you won't be able to change anything in the theme, but instead you can copy the file you want to change into your Hugo site's ```layout/partials``` directory, and change it there.
7. If you don't have a good idea of which theme you want to use, I found an excellent suggestion [here](https://github.com/tomowang/hugo-theme-tailwind/blob/main/exampleSite/README.md).  You can download some sample content, download a _whole_ lot of themes, and just run ```hugo server -t theme_name``` a bunch of times, reviewing each one.

In general, there were quite a few times I wanted to take the whole site and start again - and several times I did - but in general you can make mistakes and correct them easily.  It just takes a little practice.
