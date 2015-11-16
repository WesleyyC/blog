---

layout: post

label: "ml"

title: "ML: My First with Parallel Computing"

published: true
---

Parallel computing is fun, but quiet different!

#### Intro

“Big data is like teenage sex: everyone talks about it, nobody really knows how to do it, everyone thinks everyone else is doing it, so everyone claims they are doing it…” — Dan Ariely

And the same quote can apply to many other related terms with big data like machine learning, deep learning, data visualization and parallel computing. Fortunately, I did get a chance to **do** one of them recently. 

#### How I Get Into This Whole Paralel Computing Business?

Over the pass summer, I have been doing some research and implement an approximate agorithm for efficient graph matching. Utilizing this algorithm, I later developed a spatial pattern matching model following the research of my mentor Prof. Hong.

Even though the graph matching runs relatively fast, it still takes about 30 mins to match two graphs with about 100 nodes and such matching needs to run several round in our model develop algorithm. As bad as it sounds, we were actually quiet happy with our progress at that point and we were able to demonstrate the viability of our model through small samples. 

I mean, every computer science problem is not a problem until we need to scale.

#### But,

Going into this fall, we decided to apply the algorithm to biology domain and aim to solve a facinating yet challenging probelm: generate a model to learn the common domain across all the sample proteins. We convert sample protein crystal structures into graphs and hope to understand the common structure in this sample protein utilizing our algorithm. This is a fascinating job. I mean, look at this beautiful matching graph:

![p-compute-1](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/p-compute-1.png)

But we run into a problem: the scaling problem. Most of the proteins have hundreds of amino acids and give us a graph with hundreds of nodes. Therefore, we need to make our graph matching faster. Since the majority time for runing the graph matching algorithm is used to build a huge matrix storing the edge compatabiltiy between all the edges of two graphs. The work can be huge once we scale. Let's say we have a graph with A nodes and another graph with I ndoes. Then there will be at most A\*A edges in the first graph and I\*I edges in the later. Therefore we will need to compute a huge matrix with size (A\*A)\*(I\*I). That's a lot of work, but luckily the computing order does not matter, so we decide to try parallel computing.

#### The Parallel Computing Toolbox in MATLAB

MATLAB has this amazing parallel computing toolbox that can help you utilizing multiple CPU on your local machien or clusters to do parallel computing by simply change your `for` loop to `parfor` loop. That sounds pretty straight forward and that's what I thought when I first looked at the tutorial.

To Be Continued ...


