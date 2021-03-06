---

layout: post

label: "ml"

title: "ML: Machine Learning and Human Learning"

published: true
---

What if we train machine learning models just like training babies?

![human-learn](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/human-learn.jpg)

####Intro

I read [an interesting comment](http://zhi.hu/o889) today about the "notorious" over fitting problem in machine learning and the author describes an "over fitted" model as a student who try too hard to learn from the presented learning material and start to believe in some materials that are not necessarily true.

![machine-learn](https://raw.githubusercontent.com/WesleyyC/blog/gh-pages/images/machine-learn.png)

I found this comment particularly interesting. Not just because it is funny, but also because it reveals a fundamental relationship between machine learning and human learning. For too long, we have been thinking about machine learning model as a statistical model, but thinking of training model as training students can be very helpful. And I think that is partially why "Deep Learning", the recent head-line machine learning technique, can be so successful.

####In Deep Learning

As we know more and more about cognitive science, people start to develop cognitive system in machine and "Deep Learning" is a great example. To perceive information from sensors, human brain has a sequence of specific -> general layers where separated signals are received in the first layer and being generalized and understood in the later layer.

For example, a combination of photon receptors gives us a shape of green tree and then memory system helps us remember this shape is "a tree". Similarly, in deep learning, information, like images, are broken down and recombined in higher dimension before being learned. However, I don't think "Deep Learning" is the only reflect of human's learning/cognitive process.

####In Older Machine Learning

Even though in older machine learning field, building model is more of a statistical process, they are still very well related to human learning process.

#####Work Harder on Your Weak Spot

When I was still in high school, we were ranked by our total score of Chinese, Math, English, Physics, Chemistry and Biology. I seldom made the top 10 because I am not very good at Chinese and Biology. Therefore, I spend more time on Chinese and Biology. Work harder on your weak subject, that's what they call.

The same spirit is actually borrowed by a machine learning method called AdaBoost, where a number of models is being trained and at each training iteration, the sample that is not correctly predicted will be given more weight so that the model will learn from this sample harder during the next iteration. So yes, the model needs to work harder on their weak sample/feature too.

#####Don't be the Frog that Lived in the Shallow Well

When I was very little, my parents liked to travel with me so that I can see more and hopefully understand more. They also encouraged me to experience different things because they believe to be creative, you have to see more and understand how huge this world can be. That famous frog from Aesop's Fables thinks the sky is just a blue circle because he hasn't seen much.

In machine learning, seeing more means more sample data. To train a good model, we emphasize on collecting data and there is a even motto call "Who owns the data, who is the king." in the field. Only with enough training sample, a model can be robust enough. If the machine only has learned imagines of Caucasian and gorilla, of course it will label African Americans as gorilla (Joke is on you, Google!). So yes, you don't want your machine learning model to be the frog that lived in that shallow well.

#####Don't memorize the practice exam (or you are over fitted)

I love professors who are willing to prepare practice exams even though memorizing every single questions in the practice exam will NOT get you anywhere. I think a good approach for studying practice exam is just getting a basic understanding of what will be in the exam and how hard the exam will be. Moreover, I would like to get a feel on how the professor will test on a specific topic, and what will be the best approach for questions on this kind of topic. So, instead of learning the detail of the practice exam, grepping a general idea from the practice exam can be more helpful.

If we think of the training sample in machine learning just as practice exam, and doing sample exam as training a model, the same spirit applies too. If the machine just memorizes every single questions (data point) from the practice exam (training data set), it will be over fitting the training data set (just like the over fitting sample above!). Even though the model score 100 points in its sample exam, memorizing every single exam will probably not able to help it pass the actual test (test sample). Instead, if the model can make a good generalization of the training sample, it probably can make a 80% during the actual test even though it can't really tell the specific answer for those practice questions.

####Conclusion

The cliché study strategy list can go on and on, but the idea behind these examples is really about relating machine learning idea with human learning strategy and maybe next time, when you are training a model, think of it as training a student. What will you do?

Many good machine learning researchers tend to be very good mentors and I wonder if this idea has anything to do with that. ;P

######Disclaimer: I don't have a Ph.D in machine learning or cognitive science, so ...


<!-- This summer I was working on a machine learning model that is able to summarized pattern from sample images. In the model, there are multiple components and each component represents a single pattern that are similar to the pattern I want to summarized, the model pattern.  

During the development, I imagine the training process just like parents teaching their little baby what a rabbit is and each component will just be a image label the little baby create for recognizing rabbit. When parents points to something and point to a little rabbit, an image sample is store in baby's memory system. So after meeting many Mr.Bunny, our little baby will have a lot of sample of environment with rabbit. -->
