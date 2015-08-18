---

layout: post

label: "ml"

title: "TOOL: Parse for Android Development and More"

published: false
---



####Intro

Building backend server and database can be a lot of work in the old day. Even with package like Node.js, build up API for database can be unpleasant. Moreover, for mobile application, "back threading" the internet calls and manage them in weak signal condition can be pains in the ass.

However, in the past month, I have built two Android applications with server database and server calls handled properly. These are made possible by a service called Parse.

![parse](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/parse.png)

Parse is a backend service developed by Facebook for Android/iOS/Web developer to build their database, monitor service status and "cloud" their code.

"Wikipedia"

####Parse with Android Development

With the documentation on Parse, it is very easy get started with the Parse backend and the SDK is well documented so it is very handy and I am not going to go over it here. However, I do want to high highlight some useful features:

#####Query Adapter

In android development, if you have a list of items want to display, for instance a list of contacts information, you can use something called adapter where you can bind your data to the UI element

Traditionally, what I would have done is make a server call to get the data I want to display and then bind the data to the view in the adapter. This will involve building my own adapter and manage all the server call.

However, in the Parse SDK, there is something called Query Adapter where you can simply create a server database query and make a query adapter out of it so that you don't need to worry about managing the server calls. If you want to customize the binding activity, you can simply extend this query adapter and do whatever you want with the data.


#####Parse Image View

If you want to display a image in our Android application, we can create a image view and bind an image to this view. If the image is on the server, we will need to download if from the server. Since image can be very large somtime, we will want to do the download in the back thread. However, since the image view binding is happening in the main thread, things get tricky very quickly.

To help with that, Parse SDK has its own Image View where you can simply cast a normal Image View to parse Image View and bind your image query on this view. Then it will help you load the image in background and display it on the image view without dragging down your main thread activity.

#### Why Parse?

I think Parse is amazing because it helps developer, especially for start up, to focus more on building the application itself instead of spending a lot of time to build or manage their own database.

Moreover, it is very user friendly. As I mentioned, in the SDK, there are not just classes 
