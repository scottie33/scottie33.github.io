---
layout: post
title: "Markdown I learned so far"
description: "Markdown Notes"
category: Coding
tags: [markdown, html, coding]
---
{% include JB/setup %}

So far, what I know about markdown. Please follow me if you're interested.

## The following code is easy, have fun =)

----

Here we start, the ***first line*** is,
(please be noted that every code line you want it to only display, or say, not to be transcripted by markdown, 
is indented at least 4 spaces)

	<http://scottie33.github.io>

you will get: <http://scottie33.github.io>

	<genius@github.com>

you will get: <genius@github.com>

---

When you want to throw out some ***text with link***, e.g., 
	
	[www.google.com](http://www.google.com)

you will get [www.google.com](http://www.google.com). and more, 

	[www.google.com](http://www.google.com "go to google and dig something out to eat, pal")

you will get [www.google.com](http://www.google.com "go to google and dig something out to eat, pal") (***put your mouse on the link. oh, don't click it, just put it there =)***)

Or, ***alternately***, may you type this:

	[www.github.com][] is the link we want to go to.

       [www.github.com]: http://www.github.com (this line can not be indented more than 3 spaces to take effect)

[www.github.com][] is the link we want to go to.

   [www.github.com]: http://www.github.com

You may also ***try this way***:

	[google][1] is better than [bing][2]

	   [1]: http://www.google.com "better"
       [2]: http://www.bing.com "worse"

[google][1] is better than [bing][2].
	
   [1]: http://www.google.com "better"
   [2]: http://www.bing.com "worse"

---

No, I am not just saying it, since it's the truth: 
	
	*[google][1] is better than [bing][2]* (*italic*);

*[google][1] is better than [bing][2]* (*italic*);

	**[google][1] is better than [bing][2]** (**bold**);

**[google][1] is better than [bing][2]** (**bold**);

	***[google][1] is better than [bing][2]*** (***bold & italic***);

***[google][1] is better than [bing][2]*** (***bold & italic***);

	_And "_" also has the same effect here just as "\*"._

_And "-" also has the same effect here just as "\*"._

---

Then we show some sentences here, one by one:

	> Hi there, how have you been?

> Hi there, how have you been?
	
	> Good, good, how about *you*?

> Good, good, how about *you*?

	Title
	=====

Title
=====

	Title
	-----

Title
-----

	--- (a split line)

---

	---- (a split line too)

----

	***** (still, a split line)

*****

	****** (WTH, a split line)

******

	- - - - - (Gsf!@$#%^Q@, a split line ... )

- - - - - 
	
	* * * * * * (... anyway, they are all split lines ...)

* * * * * *


	##### small title
	#### medium title
	### large title
	## very large title
	# huge title

##### small title
#### medium title
### large title
## very large title
# huge title

-----

----

Eh, ***finally*** we are about to end this, tired? alright, here's a photo of [**Naomi Watts**](http://www.imdb.com/name/nm0915208/), check it out:

	![I am an image](http://somewhere.jpg "I am an image")

![I am a image](http://image.qpicture.com/image/n/artist-naomi-watts/naomi-watts-384599.jpg "I am an image")



