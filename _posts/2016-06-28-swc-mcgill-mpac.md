---
layout: post
title: Software Carpentry Workshop Post-Mortem
---

Recently I have been involved as an instructor in two [software-carpentry](http://www.software-carpentry.org) workshops. For several reasons neither of these workshops felt like the traditional SWC workshop. This post aims to layout some of the differences and highlight some of lessons learnt.

Comments on this post can be made [here](https://github.com/tomwright01/tomwright01.github.io/blob/gh-pages/_posts/2016-06-28-swc-mcgill-mpac.md).

**Tl;dr**
* Communication with the hosts is essential, they often have different expectations for the workshop that the instructors.
* Tailoring examples and lesson content to the learners domain pays off with increased motivation and removes cognitive load.
* Seeking regular feedback from learners allows you to adjust contest as the workshop proceeds.
* Avoid rushing material because you think participants will find it too easy, removing it completly is better.
* The new SurveyMonkey post workshop survey is excellent, many thanks to everyone involved.

# Workshop 1

## Background

The audience for the workshop was described as 3 research groups, all involved in medical image processing (mainly MRI). This really interested me as I'm doing a fair amount of image processing as part of my job and I was looking to make contacts and gather ideas. The host was looking for a python based workshop. We were a little worried about the level of existing knowledge in the participants, we were assured the participants had excellent programming knowledge mostly in Matlab. Most SWC workshops have a wide range of knowledge but in my experience the knowledge level is more biased towards beginners.

The host seemed to have a lot invested in the workshop being considered a success, before the workshop started several questionaires designed to assess pre-existing knowledge were circulated; I don't think the SWC pre-workshop questionaire was ever used. As expected the responses were all over the place.
As a final wrinkle the host wanted to integrate the workshop with a _hackathon_. Participants were to work in teams on a couple of _real world_ image processing problems. We were invited to join in these sessions, which were run after each day's teaching was completed, to act as advisors. This integration meant the workshop ran over 3 days instead of the usual 2.
The range of participants was the broadest I have ever seen, undergraduates to senior post-docs with backgrounds in clinical neuroscience to computer science, no lecturers / investigators though! One group of participants were wearing t-shirts advertising a professional quality python library that is hosted on Github and is developed and supported by this lab.
I am sure some of the participants were at least as familier with the material as we were, however it quickly became obvious than some were complete novices. With a couple of significant exceptions the participants were all very receptive.

## Content

We decided to cover [Shell](http://swcarpentry.github.io/shell-novice), [Git](http://swcarpentry.github.io/git-novice) and some custom python material drawn from [here](https://paris-swc.github.io/advanced-numpy-lesson/) with added material based on the [Intermediate-Mosquitos](https://swcarpentry.github.io/python-intermediate-mosquitoes/) parallel processing lesson.

**Shell** went OK. Following a suggestion on the Discuss mailing list I started by having learners `git clone` a repository with the example file system. This worked really well and avoided all the usual problems with downloading and unpacking the zip file. Because of the perceived expertise of the participants I rushed the content, particularly skipping a lot of the exercises. In hindsight this made for a fairly boring session which the participants didn't really enjoy. I think the exercises would have helped some of the less experienced users develop confidence. Feedback did focus a lot on the lack of hand-on exercises, but one comment that I found gratifying came from one of the more advanced users who stated "I am really experienced in using the shell but the material made me think about how it can be used to develop workflows"

**Git** was split over two sessions, in the first we covered local repositories and in the second collaboration with GitHub. Again following a suggestion on Discuss I used the concept of a recipe for the collaboration episode. I can confirm this works really well. An interesting comment that came up in feedback was "Why do we teach dealing with merge errors, would be better to teach strategies to avoid them".

**Python** had it's ups and downs. We tried to teach the early material using a `Virtual-Env`. Although instructions had been circulated for setting up an environment not enough time was allowed to go through this in detail. Some participants failed to get it working which led to significant frustration, in addition I don't think some participants really understood the benefits. For the parallel-processing lesson I modified the example lesson to use a domain specific example, processing a video where a transform was performed on each frame. The lesson works through the stages of building a working application resulting in a final python [script](https://github.com/tomwright01/imp-parallel/blob/master/normalise_movie.py).

**Capstone** We had a bit of time left on the last day, so I decided to try a capstone exercise. I really wanted to demonstrate the potential of the [Juypter notebook](http://jupyter.org/) for reproducible reporting. I created a [blank notepad](https://github.com/tomwright01/imp-parallel/blob/master/ConeCounting.ipynb) with a task and a few suggested functions. Participants worked in small groups and had to consult the documentation for the functions to complete the task. Because participants were already very familer with `git clone` it was easy for me to quickly distribute this notebook. In addition I later uploaded a [completed example](https://github.com/tomwright01/imp-parallel/blob/master/ConeCounting-Complete.ipynb) which participants could `git pull`.

## Observations

Although running in parallel with the hackathon made scheduling more difficult and made for long days, the synergy between the two exercises was good. Many of the groups presented thier solutions using Juypter notebooks and hosted the code they had developed on GitHub. The software-carpentry component was not completly voluntary for the participants and that caused problems, a (very) few participants were not convinced by the live coding approach, however it was interesting to see there were some real converts.

# Workshop 2

## Background

Another interesting audience. This time it was a group of data analysts from a professional organisation. The participants were used to working in SPSS and SAS with a couple having experience with R.
The hosts were keen to have the lessons tailored to thier domain and provided us with a sample dataset that the participants were used to seeing. Unfortunately this data was provided under a non-disclosure agreement so the lesson material will need some modification before I can make them available. The hosts were very keen to cover integrating R with databases.
This was to be a standard 2 day workshop (9:30 - 4:00) however at the last minute we were informed that we would lose a whole morning session.

## Content

[Shell](http://swcarpentry.github.io/shell-novice) and [Git](http://swcarpentry.github.io/git-novice) were taught by James Desjardins, partially due to the time constraint and partly because we didn't feel it would be relevent to the learners we only covered local Git in detail. James covered the potential of git for collaboration. Feedback on both these episodes was excellent with most respondents indicating increased knowledge, reduced intimidation and increased interest in learning more.  

I taught a severly hacked version of the [R for reproducible scientific analysis](http://swcarpentry.github.io/r-novice-gapminder) material. The plan was to cover data manipulation with R leaving out all the more traditional material on writing code (functions, for loops, if statements etc.). Working with realistic data and talking with the hosts enabled me to identify many of the tasks the participants would require. For example the data contained a lot of date fields and I was able to cover date handling in R in some detail. In addition using the real data enabled me to highlight some real world problems such as missing values coded in multiple ways (0, 99) and date fields set to 1582-10-14 (the epoch date for SPSS). In addition participants quickly started asking relevent questions such as "how do I identify records where the completed date is earlier than the start date?"
The cutdown version of the gapminder material worked really nicely, missing out large chunks didn't interupt the flow of the lesson. In general I covered lesson 1-5, 8, 13 which I think is closer to the [Data Carpentry](www.datacarpentry.org) approach which I am very keen to investigate further.
During the lesson I demonstrated developing code in the console window of RStudio and copying useful bits into a script file. I had intended to use this approach to get the participants to convert the script file into a [knitr](http://yihui.name/knitr/) document, unfortuantely due to the time constraints I had to skip this as an exercise but could show them a completed knitr document. Because they were familier with the code chunks used I think it was a good example for demonstrating the power of knitr for reporting.

# Conclusions

Communicating with workshop hosts enabled us to tailor these workshops to a wide variety of learners resulting in several positive outcomes including increased motivation and reduced cognitive load. The existing lesson materials make an excellent starting point for customised lessons, however the customisation process still requires a large amount of time. Seeking regular feedback and having materials hosted on GitHub enabled changes to be made during the workshop, again this required significant effort from the instructors.
