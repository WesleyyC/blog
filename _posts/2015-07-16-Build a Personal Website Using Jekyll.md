---
layout: post
title: "{TOOL}Build a Personal Website Using Jekyll"
published: true
---


I was wandering at Github last night at around eight and I saw Kahlil forked a project called [Jekyll-now](https://github.com/barryclark/jekyll-now). I clicked in it out of curiosity and 12 hours later, this is what I got. 

![Personal Website](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/personal_site_screenshot.png)

Since I don't have much time to go into detail

### I. So what is Jekyll?

> Jekyll is an open source program, written in Ruby by Tom Preston-Werner, GitHub's co-founder. Jekyll is a simple, blog-aware, static site generator for personal, project, or organization sites. Instead of using databases, Jekyll takes the content, renders Markdown or Textile and Liquid templates, and produces a complete, static website ready to be served by Apache HTTP Server, Nginx or another web server. Jekyll is the engine behind GitHub Pages, a GitHub feature that allows users to host websites based on their GitHub repositories.
We loved with a love that was more than love

Basically, Jekyll is a static webpage server. But it is special in two things:
- It is not a traditional HTML/CSS/JavaScript framework as your data is not populated by direct JavaScript command. Instead, your data is stored in a Markdown file with simple tag and then you use Liquid templates to populate the content in the Markdown files. Since we want to build a personal page with introducation to your profession experience/ projects etc, each one of your markdown file can be 
- Since Jekyll is supported by Github repo, you don't need to get a dedicated server for your personal page. Instead, you can simply use github.io to serve your jekyll sites.

### II. Install Jekyll

If you are running Mac OSX, where Ruby should be already installed, you can simply do 
	gem install jekyll
in your terminal window and Jekyll will be installed automatically.


### III. Start with a Template




