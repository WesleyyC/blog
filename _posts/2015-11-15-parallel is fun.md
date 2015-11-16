---

layout: post

label: "ml"

title: "ML: My First with Parallel Computing"

published: true
---

Parallel computing is very dcifferent, yet super fun!

#### Intro

Building backend server and database can be a lot of work in the old day. Even with package like Node.js, build up API for database can be unpleasant. Moreover, for mobile application, "back threading" the internet calls and manage them in weak signal condition can be pains in the ass.

However, in the past month, I have built two Android applications with server database and server calls handled properly. These are made possible by a service called Parse.

![parse](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/parse.png)

Parse is a backend service developed by Facebook for Android/iOS/Web developer to build their database, monitor service status and "cloud" their code.

#### Parse with Android Development

With the documentation on Parse, it is very easy get started with the Parse backend and the SDK is well documented so it is very handy and I am not going to go over it here. However, I do want to high highlight some useful features:

##### Query Adapter

In android development, if you have a list of items want to display, for instance a list of contacts information, you can use something called adapter where you can bind your data to the UI element

Traditionally, what I would have done is make a server call to get the data I want to display and then bind the data to the view in the adapter. This will involve building my own adapter and manage all the server call.

However, in the Parse SDK, there is something called Query Adapter where you can simply create a server database query and make a query adapter out of it so that you don't need to worry about managing the server calls. If you want to customize the binding activity, you can simply extend this query adapter and do whatever you want with the data.


##### Parse Image View

If you want to display a image in our Android application, we can create a image view and bind an image to this view. If the image is on the server, we will need to download if from the server. Since image can be very large somtime, we will want to do the download in the back thread. However, since the image view binding is happening in the main thread, things get tricky very quickly.

To help with that, Parse SDK has its own Image View where you can simply cast a normal Image View to parse Image View and bind your image query on this view. Then it will help you load the image in background and display it on the image view without dragging down your main thread activity.

#### Why Parse?

I think Parse is amazing because it helps developer, especially for start up, to focus more on building the application itself instead of spending a lot of time to build or manage their own database.

Moreover, it is very easy to use since the Parse SDK introduce not just basic RESTful service but also some handy classes like Parse Image View and Parse Query Adapter which makes it super easy for us to integrate it with Android Development environment.

#### The Idea of Abstraction

As a kind of abstraction, Parse packages the whole backend "dirty" work and presents us a very clean and easy to use SDK. Therefore, without any knowledge in building database and server, a developer can have a backend for his/her application.

In some sense, abstraction is the most important concept in computer science. Will first came up representation to abstract data, then we came up programming language that can abstract the computing process, after which we abstract a sequence of operation and call them functions, which we can operate again and again.

So we love abstraction and that's why will come up object oriented programming where we can represent data and function in a very clean manner so that user does not need to know what is in the package.

Following these ideas, we now have service like Parse and tons of API that help us create things that we actually know very little about. This allows us to build products and create features in a very effective way. Standing on giant's shoulder, we don't need to recreate the wheel anymore.

It is very cool, but maybe a little scary?


#### The "Problem"

Today, many people are worried about the increasing layers of abstraction in computer science might train a new generation of computer scientist that has very little knowledge of the fundamental mechanism of computer.

With Parse, students might be able to graduate with a CS degree without any database/server knowledge. Maybe in a very near feature, with more extra layers of abstraction, CS graduates might not need to know how to write code (people can already make games by dragging/linking modules without any coding).

This sounds pretty mess up, but I think it comes with the nature of computer science, its nature of abstraction. Computer science is very much about problem solving and once you know how to solve the problem, you can use whatever tools you like. The increasing layers of abstraction is giving us better tools to solve problem but to come up with the solution has never change.

So I probably will still take a database course and a network course, but I will keep using Parse without feeling guilty about not knowing what's going on underneath.
