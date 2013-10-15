# www.rian.me

## Usage

### Rake Tasks

`rake new_page["about-me"]`
`rake new_post["title"]`

### Generate & Preview

```
rake generate   # Generates posts and pages into the public directory
rake watch      # Watches source/ and sass/ for changes and regenerates
rake preview    # Watches, and mounts a webserver at http://localhost:4000
```

### YML Attributes

- layout: example: post|page
- title: string
    - example: "My Great Post"
- date: string
    - example: "2013-10-01 09:51"
- comments: boolean
    - example: false
- categories: array
    - example: [Octopress, Ruby, Development]


## Deployment

`rake generate`
`rake deploy`

## To Do

### Features

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

### Pages
* Create An About Page
* Create a Project page

### Posts
* ~~Octopress Cheat Sheet~~ Doing this in README.
    * ~~Rake tasks~~
    * Available languages for syntax highlighting
* How to Code Folding in Vim/MacVim

### Tags
* Octopress
* Lessons (for dev meetings)
* Vim
