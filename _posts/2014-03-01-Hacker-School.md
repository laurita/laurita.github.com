---
layout: post
tagline: The Beginning
category: 
tags: [Hacker School, NYC]
---
{% include JB/setup %}

A couple of months ago I got accepted to [Hacker School](https://www.hackerschool.com/) and as a result I am now in New York for three months. Since then I got quite a few questions and/or remarks on what I am doing here. So let me fist explain briefly what Hacker School is.

![HS](/images/hs_whole.JPG)

HS calls itself a "writers' retreat for programmers" and, frankly, it really describes the atmosphere very well. It is a place which gathers around 45-70 trully passionate programmers for 12 weeks into one place and allows to develop themselves in various ways with the same aim in mind - to become a better programmer. For some it means hacking Linux kernel, for others developing a game in JavaScript. But no matter what you are doing, you are doing it because it is fun. Not because your boss told you, not because a customer needs some feature fast, not because the school assignment requires that, but because you want to do it. And that is the key to success!

![Rules](/images/rules.JPG)

There are not many rules here. Actually, probably just four.

**1. No feigning surprise** It discourages one to say such things as "OMG! How can you not know what a virtual machine is???"

**2. No well-actually's** It asks you to keep your tiny little correction if it is a detail of low importance which interrupts an otherwise almost correct development of one's thoughts.  

**3. No back-seat driving** If you want to help or offer advice, please do it fully engaged instead of sporadically interfering from the other side of the room.

**4. No subtle sexism** No subtle sexism, racism, homophobia, etc.

Pretty simple!

![HS](/images/hs_whole2.JPG)

There are 50 people in this batch of Hacker School. 14 of them are girls. And they are all smart and motivated and trully inspiring. They say that this time they have less. However, for me it seems a lot.

The days at HS are never boring. They start at 10:30 with a short stand-up in groups of around 6 people. Just a couple of sentences what you did yesterday and what are you planning to do today. If you want of course you can tell others about the problem you were fighting for hours. It is highly likely that among all those 50 people somebody has already done a similar thing.

And then you go and simply do your stuff! You can pair with somebody, you can do it alone. You can ask people to review your code or offer somebody else to do the same thing. You can develop the implementation of some game which will never be used, but will be fun to code. Nobody will discourage you to write something that you are passionate about. On the contrary, many will be happy to help.

On Mondays we have the talks (plus free dinner :)). Most often they are hosted by some tech company. So far we had two talks at eBay. On the second Monday [Mel Chua](http://melchua.com/) gave a talk on [Edupsych theory for hackers](http://de.slideshare.net/mchua/edutalk-w2014). Very useful piece of information which forced me to reflect about how I learn and hopefully improve and speed up this process. Mel stayed at Hacker School for one week and helped everybody with the learning issued.

The second Monday [Evan Czaplicki](https://github.com/evancz) presented his designed and developed language [Elm](http://elm-lang.org/) - an awesome functional language for the Web that compiles to HTML, CSS, and JavaScript. Evan definitely raised the bar of the Monday talks. Everyone was impressed by the expressiveness and conciseness of a language, not to talk about the fun that you get developing games in it.

During the week we usually have some residents at Hacker School. They are people who come to HS for one or two weeks and share their knowledge directly with the students. You can talk to them, ask for advice or just listen and become smarter by simply doing it. I had an apportunity to talk to Evan about testing the reactive programs. It still seems like a pain in the ass for me, especially if the actors are distributed remotely.

Besides Evan and Mel, we had [Greg Price](http://web.mit.edu/~price/) as a resident for one week. He is a kernel developer and a systems programmer. Also knows a lot about programming languages. He gave a talk on [What is that process doing?](http://price.mit.edu/tracing-w2014/#1) which was super useful. He showed two main ways how to discover the relevant places in the code that you did not write and to understand them.

1. From outside:

	*	`/proc/$PID/` - snapshot info
	*	`lsof` - another view of `/proc/*/`
	* `strace` - interactions over time
	* `tshark` - network interactions

2. From Inside:

	* `perf`
	* `gdb` (and `pdb`)

[Stefan Karpinski](http://karpinski.org/) was a resident this week. He is a developer of [Julia](http://julialang.org/) - functional dynamic programming language for technical computing.

Tuesdays and Wednesdays for me are the days when most of the work is done. On Thursdays we have presentations of what the hackerschoolers have done. There were pretty nice things presented already such as [PSGPlay](https://github.com/deckman/psgplay), [msp](https://github.com/adwhit/msp), [pairjam](https://github.com/neerajwahi/pairjam), [Little Lisp](https://github.com/maryrosecook/littlelisp) and many others. Then on Thursdays there is a game night when the alumni can join the current batch and play poker or board games. Last week I tried a game called [Love Letter](http://www.alderac.com/tempest/love-letter/).

And then there are Fridays during which we practice the things that are useful for job interviews. Last week we implemented hash tables, analyzed the various strategies of collision handling and so on. This week the topic was recursion. I find these Fridays very useful as one can choose the level at which to explore the topic.

 
































 