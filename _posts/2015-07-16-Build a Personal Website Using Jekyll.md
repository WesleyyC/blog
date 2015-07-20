---

layout: post

title: "Tool: Build a Personal Website Using Jekyll Blog Framework"

published: true
---------------

I was wandering at Github last night at around eight and I saw Kahlil forked a project called [Jekyll-now](https://github.com/barryclark/jekyll-now). I clicked in it out of curiosity and 12 hours later, this is what I got.

![Personal Website](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/personal_site_screenshot.png)

It is originally designed to create blog site, but with some creativity, we can make it a personal website ;P

### I. So what is Jekyll?

> Jekyll is an open source program, written in Ruby by Tom Preston-Werner, GitHub's co-founder. Jekyll is a simple, blog-aware, static site generator for personal, project, or organization sites. Instead of using databases, Jekyll takes the content, renders Markdown or Textile and Liquid templates, and produces a complete, static website ready to be served by Apache HTTP Server, Nginx or another web server. Jekyll is the engine behind GitHub Pages, a GitHub feature that allows users to host websites based on their GitHub repositories. We loved with a love that was more than love

Basically, Jekyll is a static webpage server. But a very special one:

-	It is not a traditional HTML/CSS/JavaScript framework as your data is not populated by direct JavaScript command. Instead, your data is stored in a Markdown file with simple tag and then you use Liquid templates to populate the content in the Markdown files. Without a database, a ordinary blogger can update his/her blog by simply adding a new markdown file without worrying the code.
-	Since Jekyll is supported by Github repo, you don't need to get a dedicated server for your personal page. Instead, you can simply use github.io to serve your jekyll sites.

And the Jekyll-now I mentioned above is a even simpler version of Jekyll that already have a blog layout and all you need to do is changing web title and adding markdown files.

### II. Install Jekyll

If you are running Mac OSX, where Ruby should be already installed, you can simply run

```
gem install jekyll
```

in your Terminal and Jekyll will be installed automatically.

### III. Start with a Template

Just to get started without worrying too much about css/javascript, you can go to some of the template website to get started with a beautiful template. The one I use comes from [Start Bootstrp](http://startbootstrap.com/template-overviews/landing-page/). I love this site because their template are all built with Bootstrap, so it is very easy to add animation effect/navigation bar/responsive layout, etc.

From here, you can choose to download the Jekyll version of the template. After you unzip the file, navigate into the foler storing all the template files in Terminal.

If you successfully install jekyll, you should be able to run

```
jekyll serve
```

in Terminal and it will compile our jekyll project into a _site folder and serve our website through this folder). Go to this address [http://127.0.0.1:4000/](http://127.0.0.1:4000/) in your browser and you should be able to see the starting Template.

### IV. Personalize

##### Basic Config

First, you can start personalize the website by changing the titile/ subtitle/ author/ social info by overwritting the _config.yml and index.html, where these informations are stored.

##### Understand the layout

Then you can go into the _layouts folder and opens up the default.html file.

```HTML
	<!--liquid signs are removed for parsing-->
	<body>
		include header.html
		include about.html
		include page_content.html
		include contact.html
		include footer.html
		include js.html
	</body>
```

In the body segment, you can findout how the webpage is composed. You have a header file represetns the banner and the open image. An about file introduce yourslef, a contact file create the contact banner in the end, and a footer file with the website information. The js file is for all the javscript you are inserting for the website. If you are not please with any of the components, you can just go to these files (located in the _includes folder) and change them directly.

If you want to add some components, for our purposes, a page content for experiences, a page content for projects and a page content for eduction record, you can create different page_content html file in the _includes folder and add/reordere them here in the default.html.

##### Populate Contents

But there is one thing we haven't talked about, is the page_content file. This file is the main file that will interact and populate your markdown files in the _post folder. Even though there is only one page_content file, it can populate all the markdown files in the _posts folder using a Liquid Template:

```HTML
<section id="services">
<!-- Page Content -->
<!--liquid signs are removed for parsing-->
for post in site.posts reversed
  capture thecycle | cycle 'odd', 'even' | endcapture
     if thecycle == 'odd'

```

In the header of this page_content file, we can see there is a for loop, wichi will represent each file as `post` and go through each of our files in the _post folder and generate a html section for each of them.

In our case, there is also a `thecycle` variable which will help up create differnt layout for odd number post or even number post.

And then let's look at one of the markdown file that we are posting

```
---
layout: default
img: ipad.png
category: Services
title: Death to the Stock Photo:<br>Special Thanks
description: |
---
  A special thanks to [Death to the Stock Photo](http://join.deathtothestockphoto.com/) for providing the photographs that you see in this template.  Visit their website to become a member!


```

in the lines between `---`, we can see there are some properteis are defined. For example, which category this posts belonged (experiences, projects, educations?), what images are associated with it, what title is it, etc.

But how do we access this information? Let's look at the HTML file,

```HTML
<div class="col-lg-5 col-sm-6">
	<hr class="section-heading-spacer">
	<div class="clearfix"></div>
	<h2 class="section-heading">{{ post.title }}</h2>
	<div class="lead">{{ post.content }}</div>
</div>
<div class="col-lg-5 col-lg-offset-2 col-sm-6">
	<img class="img-responsive" src="img/services/{{ post.img }}" alt="">
</div>
```

as we can see, we can access the content (anything below the `---`) and the file properties by simply calling `{{post.SOMETHING}}` and we can then cooporate our content with our html/css layout, and to access the image, we just go to the img/services folder and find the image with the right name associated with the post.

One minor thing on the markdown file, since Jekyll is designed to populate blogs instead of personal info, its markdown file names has to format like YEAR-MONTH-DAY-FILENAME, so if you will still need to meet to format even though your markdown file is your resume content instead of blogs.

### V. Go Public

Once you finish testing your personal webpage at local, you can public your site through Github.

You first go to your github account and create a github repo called

USERNAME.github.io

and then you can push all your contents to this repo and your website should be live at USERNAME.github.io a couple minites later.

P.S. For those of you does not have any experince with Github, please check out this link: [http://lifehacker.com/5983680/how-the-heck-do-i-use-github](http://lifehacker.com/5983680/how-the-heck-do-i-use-github).

### VI. Conclusion

In general, I think the Jekyll framework is very easy, so if you have some expreince with web design, it should just be a piece of cake and what makes it amazing is that you just need add a markdown file to update your site. However, since the site is static, it is hard to use it to do interaction with user. So if you just want to simple way to present something, especially things that should populated in a similar way, Jekyll is definitely your way to go.

Writing tutorial is harder than I thought and I should do a better job in explaning things. Let me know if you have any further qeustions or find any mistakes in the post.
