---
layout: post
comments: true
tags: Octopress
published: false
---

* Easy Deployment
* Posts in Markdown
* Beautiful code sharing
* Better than Jekyll
* Easiest platform for me to blog

## Easy Deployment

Destinations can be to **any server** (rsync'd) , **Heroku**, or
**Github Pages** (my personal preference). For more details on each type
of deployment, head over to [Octopress'
documentation](http://octopress.org/docs/deploying/). Since I prefer
Github Pages, I'll show you how easy that is.

1. Create a GH repository in the format of username.github.io. Since my
   Github username is `rianrainey`, my repository name is
`rianrainey.github.io`.
2. Setup your project to work with Github with this command:

```
`rake setup_github_pages`
```

3. Generate, commit, push, deploy and more magic with this command

``` 
rake generate
```

4. Deploy to Github
{% codeblock %}
rake deploy
{% endcodeblock %}

In a few minutes your site will be live at username.github.io, or
rianrainey.github.io.

To deploy your blog posts and any other changes, you only need to run
`rake deploy` and you're done.


## Beautiful Code Sharing

I'm excited to be able to share code as easily as this:

``` bash How To Create a RVM Getset and .rvmrc For A New Project
rvm --rvmrc --create gemset 1.9.3-p362@octopress
```

``` ruby What Ruby Would Look Like
def my_function
  puts "Hello World"
end
```

There is an entire [Octopress page](http://octopress.org/docs/blogging/code/)
dedicated to code styling.

## Better Than Jekyll

#### Reasons Why I Chose Octopress over Jekyll

* SASS
* RSS Feed
* Archives
* 3rd Party Integration Out of the Box
    * Github - List your github repositories in the sidebar
    * Twitter - Add a button for sharing of posts and pages on Twitter
    * Google Plus One - Setup sharing for posts and pages on Google's plus one network.
    * Pinboard - Share your recent Pinboard bookmarks in the sidebar.
    * Delicious - Share your recent Delicious bookmarks in the sidebar.
    * Disqus Comments - Add your disqus short name to enable disqus comments on your site.
    * Google Analytics - Add your tracking id to enable Google Analytics tracking for your site.
    * Facebook - Add a Facebook like button
* [Additoinal 3rd Party Plugins](https://github.com/imathis/octopress/wiki/3rd-party-plugins)

Yes, I could get all of these things if I added them manually. But why? I could have a completely custom site if I just wrote it in raw HTML/CSS/JS. Why reinvent the wheel when I already want these features or will possibly want them in the future?
