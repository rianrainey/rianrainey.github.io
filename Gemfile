source 'https://rubygems.org'
ruby '2.1.3'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem 'jekyll'
gem 'jekyll-sitemap'
gem 'github-pages', versions['github-pages']
gem 'rake'
