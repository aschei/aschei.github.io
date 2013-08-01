---
layout: post
title: "Blog on GitHub using Octopress"
date: 2013-08-01 01:54
comments: true
categories: 
---
Today, I have stumbled upon a blog that uses [Octopress](http://octopress.org). It looked very clean, and I read something about Octopress and it's concepts.

It seemed similar to my current blog setup, meaning that it produces static pages out of the sources, that can then be transferred to the web server and be served very fast and easily.

Octopress also offers easy integration with [Github Pages](http://pages.github.com/). Github Pages is a hosting service of Github that is coupled to a GIT repository on GitHub. Just push changes to the GIT repository, and within seconds the changes are reflected on the respective site.

My repository is located [here](https://github.com/aschei/aschei.github.io), and the site can be viewed [here](http://aschei.github.io).

A cool concept octopress makes use of is to keep sources and the generated results in the same repository by using branches. Sources are committed to branch ["source"](https://github.com/aschei/aschei.github.io/tree/source), while the result is committed to ["master](https://github.com/aschei/aschei.github.io/tree/master). The two branches contain conceptually completely different artifacts, and they will never get merged.

The whole setup is really easy to make and it is a joy to work with it.
