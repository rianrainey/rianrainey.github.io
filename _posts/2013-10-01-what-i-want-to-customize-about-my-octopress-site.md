---
layout: post
title: "What I Want To Customize About My Octopress Site"
date: 2013-10-01 09:51
comments: true
tags: Octopress
published: false
---

## Features

* ~~Move from rianrainey.github.io to rian.me~~
* ~~Create a minimal theme and contribute it~~
    * For now I like [Slash](http://zespia.tw/Octopress-Theme-Slash/)
    * Hopefully I'll add a fly-out mobile menu later
* ~~Add my favicon~~
* ~~Implement Tags~~
    * Found out their actually called just Categories. You just add it
as data at the top of your post, like so: 

```
---
layout: post
title: "What I Want To Customize About My Octopress Site"
date: 2013-10-01 09:51
comments: true
categories: [Octopress]
---
```
 
* Add image next to Google Results
* ~~Add Google Analytics~~
* ~~Add Meta Description, Data, etc~~
* ~~[Github Flavored Markdown using
RedCarpet](http://yangsu.github.io/blog/2012/10/11/using-octopress-with-github-flavored-markdown-redcarpet/)~~
    * ~~Add Github-esque anchor links to H1-H6 headers~~
        * it just adds 'ids' to the header tag and doesn't make them links.
        * I did this through changing the Markdown engine to RedCarpet but
    * Add Checkbox ability
        * [ ] should display an empty checkbox
        * [x] should display a completed checkbox
        * I currently don't know of any open issues trying to get this
functionality implemented.
* Add JS that opens external links in new windows
    * inject it as a gist so I can keep it updated.
* Add 'Fork Me On Github'
* Style codesnippets
    * Title Bar
    * Indentation
    * Figure out how to hide line numbers. (linenos:false doesn't work)

## Pages
* Create An About Page
* Create a project page

## Posts
* Octopress Cheat Sheet
    * Rake tasks
    * Available languages for syntax highlighting
* How to Code Folding in Vim/MacVim

## Tags
* Octopress
* Lessons (for dev meetings)
* Vim
