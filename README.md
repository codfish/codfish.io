# My Personal Site

From github's [Using Jekyll with Pages instructions](https://help.github.com/articles/using-jekyll-with-pages/):

> Jekyll is an active open source project, and is updated frequently. As the GitHub Pages server is updated, the software on your computer may become out of date, resulting in your site appearing different locally from how it looks when published on GitHub.

## Prerequisites

See [Jekyll's installation guide](https://jekyllrb.com/docs/installation/).

**Summary:**

- Install Ruby, v2 or above (I use rbenv to manage ruby versions) - https://www.ruby-lang.org/en/documentation/installation/

- RubyGems (typically installed with Ruby) - https://rubygems.org/pages/download

- Mac OS X

- Bundler - http://bundler.io/


## Quick Start (local development)

1. Clone this repo

    git@github.com:codfish/codfish.github.io.git

2. Install (github pages & dependencies)

    bundle install

3. Build & serve

    jekyll serve
