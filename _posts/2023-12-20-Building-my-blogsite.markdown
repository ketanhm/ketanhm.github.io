---
layout: post
title:  "Hosting a free website or blog using github pages"
date:  2023-12-20 12:20:26 -0700
categories: [Personal]
tags: []
description: Hosting free blogsite on github.io domain
toc: false
pin: 
comments: false
---

[GitHub Pages](https://pages.github.com/) are public web pages for users, organizations, and repositories, that are freely hosted on GitHub’s github.io domain. GitHub Pages are powered by Jekyll behind the scenes, so they’re a great way to host Jekyll-powered website for free.

[Jekyll](https://jekyllrb.com/) is a static site generator with built-in support for GitHub Pages and a simplified build process. Jekyll takes Markdown and HTML files and creates a complete static website based on your choice of layouts. Jekyll supports Markdown and Liquid, a templating language that loads dynamic content on your site.

Adding a Jekyll theme to your GitHub Pages allows to customize the look and feel of your site. 

![Building my blog](https://ketanhm.github.io/images/Build-blog.png){: w="700" h="400" }

You can preview your changes first locally and test the website. 
A custom GitHub Actions workflow triggers the workflow (typically by a push to the default branch) to generate site automatically, when a new push is triggered. 


