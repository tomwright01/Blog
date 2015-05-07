---
layout: post
title: Presentations with reveal.js
---

I needed to give a presentation recently, the topic was ["writing a scientific paper"](http://blog.tomwright.ca/writing-a-scientific-paper).
Not the most exciting topic so I decided to use it as an excuse to get familier with [reveal.js](http://lab.hakim.se/reveal-js).

I'm very glad I did.

In case you're not already aware, Reveal.js is framework that makes it really easy to create good looking presentations using either basic HTML or markdown.

## Setup

Setup was surprisingly easy. At it's simplest you download the framework, then edit index.html

    git clone git@github.com:hakimel/reveal.js.git my_presentation
    cd my_presentation
    atom index.html

__Note:__ atom is my new text editor.

The example presentation contained in `index.html` is a comprehensive demo of whats available.

Taking it a bit further I found this [Blog](martinbrochhaus.com) by mbrochh that takes things to the next level and allows integration with [github](www.github.com).
My fork of his repo is [here](github.com/tomwright01/reveal-template).
