# Restify Documentation


## Updating the docs

To pull in the latest documentation for the project, simply:

```bash
git clone --recursive git@github.com:restify/restify.github.io
cd restify.github.io
git submodule update --remote && git add _docs && git commit -m 'bump' && git push origin master
```

And the docs will automatically rebuild themselves using [GitHub Pages](https://pages.github.com/)

## Adding doc pages

To add a doc to the website, include the appropriate header:

```text
---
title: [Page Title]
permalink: /docs/[page-id]/
---
```

Then add the page to the navbar by adding the `page-id` to the appropriate section in  `_data/docs.yml`:

For example:

```yml
...
- title: API
  docs:
    - server-api
    - [page-id]
...
```

## Running locally

You need Ruby and gem before starting, then:

```bash
# install jekyll and bundler
gem install jekyll bundler

# clone the project
git clone https://github.com/aksakalli/jekyll-doc-theme.git
cd jekyll-doc-theme

# run jekyll with dependencies
bundle exec jekyll serve
```

## Design

We used the amazing [jekyll-doc-theme by aksakalli](https://aksakalli.github.io/jekyll-doc-theme/) as a jumping off point for our website!
