---
layout: post
title: Creating a blog
---

It seems all the cool kids have one, at least those calling themselves data scientists, so I thought it time I started one for myself.

-----

I like the idea of keeping this all as text files with free hosting so when I came across [this](http://joshualande.com/jekyll-github-pages-poole/) blog post I thought I'd give it a go.

The site is hosted on [github](www.github.com/tomwright01) which uses [Jekyll](http://jekyllrb.com) to convert [markdown](https://help.github.com/articles/github-flavored-markdown/) files to html. A bunch of templates are provided from [poole](https://github.com/poole/poole), which saves me from having to make it look pretty myself.

Setup was pretty straight forward, examine my [commit log](https://github.com/tomwright01/Blog/commits/gh-pages) to see my mistakes.

* Update *

Just a few notes on issues I found with the above instructions:

1. The best way to link your blog to the poole templates is to first clone the poole templates:

    `git clone git@github.com:poole/poole.git`

    then use the we interface to create the github project that will contain your blog and link this with `git remote add`

    `git remote add site git@github.com:<username>/<username>.github.io`

    Updates can then be published with `git push site`.

2. Jekyll is very sensitive to spaces and tabs. Indenting code with tab characters instead of spaces caused the interpreter to ignore them. Equally extra spaces in the archives.md page meant that links to older posts were not rendered properly.

3. Creating a github project <username>.github.io causes this to be the default website for all your github projects, available at the url: http://tomwright01.github.io. Changes need to be pushed to the master branch. While the main page worked for project folders with different names, I couldn't get sub pages (about.md, archive.md) to work correctly for any other domain path.

