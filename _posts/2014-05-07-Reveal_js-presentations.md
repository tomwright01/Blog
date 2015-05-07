---
layout: post
title: Presentations with reveal.js
---

I needed to give a presentation recently, the topic was ["writing a scientific paper"](http://blog.tomwright.ca/writing_a_scientific_paper).
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

## Advantages

*So what's the big deal?*

1. It's text. Fully supported by git, I now get to version control my presentations.

2. No powerpoint (or presentations or keynote). I don't use windows so I haven't used powerpoint for a while. My presentation software has been [libreoffice](www.libreoffice.org) Impress for a while. It's good but has always felt a little shaky.

3. It's text. Alright for my first effort I wrote in HTML, but it could have been markdown. I like this way of working, it forces me to concentrate on content not effects.

4. Reveal.js introduces the concept of a 2 dimensional slide show. Slides can progress left to right (similar to traditional presentation software) or they can progress up and down. I __LOVE__ this concept, slideshows immediately become more dynamic, slides can be organised into topics, it makes you think about structure. I could go on even more, suffice to say, I think this is great.

5. I can publish my presentations onto the web. While other people probably arn't that interested, it means I have them accessable anywhere. Calling up a fully animated presentation onto my phone is just cool!

## Disadvantages

A few minor ones, I think more experience will help me deal with them.

1. Some knowledge of HTML and CSS is useful. Basic layouts such as lists and tables are pretty simple, but occasionally I needed finer control which meant going online and reminding myself of various CSS attributes.

2. I often ran into problems fitting content onto the page. The default font sizes are a little too large and it's hard to control the spacing between elements (see above). To be fair putting too much information on a slide is a common mistake and I should perhaps refactor some of my slides.
