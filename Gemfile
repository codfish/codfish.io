source 'https://rubygems.org'

# get currently-deployed version of github pages gem in project
require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)
gem 'github-pages', versions['github-pages']
