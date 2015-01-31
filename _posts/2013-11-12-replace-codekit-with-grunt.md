---
layout: post
title: "Replace Codekit with Grunt"
date: 2013-11-12 19:24
comments: true
tags: 
summary: It's time to replace Codekit with Grunt. Open source > Proprietary.
published: true
---

At [Centresource](http://www.centresource.com), we've been using
[Codekit](http://incident57.com/codekit/) for the majority of our
projects for over a year now. Codekit is a Mac desktop application that provides
a nice UI to help concatenate, minify and otherwise optimize your
javascript and SASS files. In our entire workflow, this is the only
non open-source piece of software we use.

For our Rails projects, this isn't a problem because the asset pipeline
does this for us. We use Codekit primarily for our Wordpress and Drupal
projects.

### Why Codekit Is Bad

Don't get me wrong, Codekit is great if you are new to SASS and/or
Coffeescript and you are in need of a tool the processes and optimizes
the output. But once you feel comfortable taking the training wheels
off, you should be looking for the best practice when it comes to
this part of your dev workflow. The following reasons why Codekit is a
bad practice will make sense to you:

1. A contributing developer will need to have Codekit watching their
   code to prevent superfluous changes to your JS or SASS.

2. It's a proprietary piece of software in an otherwise open-source
   codebase. Why use it if there are equal or better, free alternatives?

3. It assumes all developers will be using a Mac OS.

### Why GruntJS Is A Good Solution to Codekit

1. It's the hot thing right now. Check out the [Yeoman](http:yeoman.io)
   workflow.

2. It's free.

3. The open-source natures makes it customizable with tons of
   [plugins](http://gruntjs.com/plugins).

### How To Use GruntJS With Wordpress

Below is a basic run down of steps, but I recommend the [GruntJS Getting
Started documentation](http://gruntjs.com/getting-started).

```
npm install grunt-cli -g #install the Grunt Command Line Interface globally
cd ./path/to/your/app
npm init #create package.json file. Defaults are adequate. We'll change things later.
npm install grunt-contrib-sass --save-dev #add SASS preprocessor
npm install grunt-contrib-watch --save-dev #add ability to run GruntJS anytime there is a change to your app
npm install node-bourbon --save-dev #for ability to @import "bourbon" in your SASS file.
```

[Download my recommended
Gruntfile.js](https://gist.github.com/rianrainey/7443208). Be sure to
change the source and destination paths for the Uglify build parameters
for what is specific to your Wordpress application.

Refrences:

- [Node Bourbon](https://github.com/lacroixdesign/node-bourbon)
- [GruntJS Getting Started Guide](http://gruntjs.com/getting-started)
- [Yeoman](http://yeoman.io/)

