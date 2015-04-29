---
layout: default
title: Web Development
---

# Web Development

The first version of the prework we tried to assemble all of the best resources
for learning to build a web application in Rails. With our students, we noticed
that the pre-work wasn't preparing them as well as it could have. We were
missing a big opportunity. Our students expressed that the pre-work went for
breadth over depth. Rather than honing in on ruby, the meat of our curriculum,
a lot of time was spent on HTML and CSS which is an important but secondary
piece.

We strongly belive that learning should have context, and you should know what
your goals are.  Each section will address which learning objectives it will
cover, and at the beginning we expect all of you to check out the Ruby
assesment so you know what you'll be expected to do at the end.  There's an
infinite amount of things you could spend your time learning, part of the value
of the prework is that we can narrow the scope to only the most essential.  If
you can achieve fluency in the following topics we believe you'll flourish at
the Flatiron School.
## Setup

To complete these units, you will need a [Treehouse](http://teamtreehouse.com/)
and
[CodeSchool](http://www.codeschool.com/enrollments/dnFtaXFMbXROSVVqT3N1bngwWnBRUjhGc2k1Z1dEOW52cFJvZEMzRUZvRT0tLWpvUElMODBvdFhiZlA4MjE2Mlc2c1E9PQ==)
account. They
are each normally $25 a month, so figure you might spend $50-$100 depending on
how quickly you get through the material. 
[CodeSchool](http://www.codeschool.com/enrollments/dnFtaXFMbXROSVVqT3N1bngwWnBRUjhGc2k1Z1dEOW52cFJvZEMzRUZvRT0tLWpvUElMODBvdFhiZlA4MjE2Mlc2c1E9PQ==)
has created a $9 trial month for all Flatiron Preworkers. Register using that
link. Treehouse has an extended 30 day free trial through this [link](http://www.shareasale.com/r.cfm?b=456118&u=850011&m=43811&urllink=&afftrack=f). You also will need a
[CodeAcademy](http://codeacademy.com/) account which is free.

You should also have a Rails Development environment setup. There are lots of
guides for that on the internet and depending on your OS and setup, it's a bit
of a process. You could always use the cross-platform [Install Rails](http://installrails.com/).

Note to students accepted into the Flatiron School. We will provide you with an
account to treehouse and codeschool, feel free to use your own to get started,
but we cover those costs for the duration of the prework and semester.

## Thoughts

One of the challenges in learning how to code is that you probably don't even
know what you're supposed to learn. When creating this prework, we had 4 goals
in mind.

  1. **Full Stack**

  We'll present the full stack of technologies required to build a webapp from
  the ground up. We don't care if you use ERB or HAML. The web is built on HTML
  and everyone should learn it. Whether NoSQL or RDBMS, understanding the
  fundamentals of schema design and SQL is crucial. Students shouldn't shy away
  from depth. How can you be a web developer without a proficiency in these
  skills?
  2. **Linear Progression**

  The material is presented in order, going from web basics and computer
  basics, to markup, to styling, to version control, to programming, and then
  to databases and web frameworks. You learn the basics of code through Ruby
  and then finally move to Rails that builds upon the rest. Thus you start at
  the lowest level, the literal HTML the browser renders, and progress up
  through levels of abstraction until you finally get to the kitchen sink that
  is the Rails framework. As a beginner, don't try to learn Rails without
  knowing basic HTML/CSS and ruby. It's a disservice to your education.

  3. **Curated Resources**

  There is such a plethora of amazing content on learning to code. We liked the
  consistency of going to a few sources that all shared common interfaces and
  learning patterns, like videos and interactive portions. So this isn't a
  complete list of all the resources, but more a curated list of what we think
  works well together (with lots of feedback from alumni). We would love it if
  you submitted a github issue with more materials you've enjoyed.

  4. **Language Agnosticism**

  In the end, programming is about abstractions and expressions. The mechanics
  of code are universal and exist in all modern languages, like python, ruby,
  and javascript. We teach Ruby because we love it. Thinking your language
  choice, especially as a beginner, matters, is like thinking that you can only
  write poetry in English and not in Spanish. Obviously the beauty of poetry is
  in rhyme and meter, in metaphor and simile, in cadence and rhythm, not in the
  king's English. Why should code be any different? At Flatiron, you're
  learning how to think, how to break problems down, how to express yourself,
  how to abstract ideas, and how to work together. We just learn that through
  Ruby.

## Learning Objectives

The goal of this tutorial is to be able to do the following:

  1. Be comfortable navigating your development environment
  2. Understand where programming skills fit into the "web"
  3. Understand what pieces make up a web application
  4. Develop a level of comfort with the most common ruby patterns in web development
  5. Understand the basics of version control and why it is used
  6. Have a basic understanding of HTML including forms
  7. Through Rails you should learn the following:
      * RESTful interfaces
      * HTTP
      * Routing
      * Where ruby fits in the web development stack
  8. Develop a comfort with basic SQL queries
  9. Have a basic understanding of an ORM, ActiveRecord
  10. Develop a basic knowledge of HTML and CSS


# The Basics

{% include web/terms.md %}

{% include general/the_command_line.md %}

{% include web/html_and_css.md %}

{% include general/git.md %}

# Programming

{% include general/ruby.md %}

# Web Development

There are many mediums, through which one can deliver applications. You can
have Desktop Applications, [Embedded Applications](http://en.wikipedia.org/wiki/Embedded_system) and Web Applications to name a
few. At Flatiron School we focus on building Web Applications.

In a previous section you built a static website using HTML and CSS. You used
markup languages to tell the browser how to render the content you were
displaying. In order to have the ability to interact with your users and store
the information they give you, we'll need to add more technologies to our
toolbelt. These technologies are usually referred to as your "Stack."

A stack usually includes the following:

  * Operating System: a collection of software that manages computer hardware
    resources and provides common services for computer programs e.g. [Linux](http://www.linux.org/)
  * Web Server: Software that helps deliver web content to a client e.g.
    [nginx](http://wiki.nginx.org/Main)
  * Database: An organized collection of data. [SQLite](http://www.sqlite.org/) for example.
  * Programming Language, like [Ruby](http://www.ruby-lang.org/)
  * A Web Framework like [Ruby on Rails](http://www.rubyonrails.org/)

We've already covered the basics of your operating system and done a brief
intro to Ruby. Now we will do a short intro to the language that is used by
most of the databases we will be using, SQL.

{% include general/sql_and_databases.md %}

{% include web/rails.md %}

# Advanced Topics

{% include general/testing_in_rails.md %}

{% include web/aesthetics.md %}

{% include web/javascript.md %}

{% include web/rails_best_practices.md %}

# About

## Credits

First, we'd love to thank all the amazing people who created these source
materials. Most of it is from CodeSchool and Treehouse, with a bit from Zed
Shaw, and some from the people at Skillcrush. Obviously there are a lot more
resources out there for learning these topics. This guide is just my current
preferences and tries to put them in a linear fashion so skills can build upon
each other. Hope it helps someone. Oh and the theme for the site was purchased
from [WrapBootstrap](https://wrapbootstrap.com/).
