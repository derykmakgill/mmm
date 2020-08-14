---
layout: post
title: All we want are the facts, ma'am
---

In these troubled times, we can all appreciate a stand-up guy like Joe Friday, the fictional _Dragnet_ detective who is best remembered for saying _"Just the facts, ma'am."_ Except he [never said that](http://www.snopes.com/radiotv/tv/dragnet.asp). What he actually said was _"All we want are the facts, ma'am."_ That's actually a much better sentiment. Be gracious when you're interviewing---let the interviewees have their say and don't force them towards one topic. When you've gathered all the data, then sort out the facts.

I've never been involved in a detective interview, but occasionally I'm interviewed by a journalist. Some publications use a quaint procedure known as _fact checking_; for example, the _New Yorker_ had [a wonderful piece](http://www.newyorker.com/reporting/2009/02/09/090209fa_fact_mcphee) by John McPhee in their Feb. 9th issue on their fact-checking process. (My favorite part was about fact-checking the absence of a comma. The phrase _"William Penn's daughter Margaret fished in the Delaware"_ implies that Penn _may_ have multiple daughters, and thus by Grice's maxim that he _does_. If you put commas around "Margaret," then the name becomes a non-essential appositive, and implies that she is his only daughter.) Journalists have been worried for at least 15 years about [the deterioration of fact checking](http://www.encyclopedia.com/doc/1G1-15359180.html); as publications cut costs, fact-checking can be an early victim.

I recently had a run-in with the fact-checkers for _Wired_ magazine. They wrote and asked me:

> <tt>Is it true that at your [ETech presentation](http://en.oreilly.com/et2008/public/schedule/speaker/2513) in March, you said, in a direct homage to George Box, "All models are wrong, and you don't need them anyway"? Is that accurate?</tt>

Great, I thought--_Wired_ is a publication with integrity and wants to get the facts right. I wrote back:

> <tt>The quote I used was "essentially all models are wrong, but some are useful".</tt>
> 
> <tt>The point I was making -- and I don't remember the exact words -- was that if the model is going to be wrong anyway, why not see if you can get the computer to quickly learn a model from the data, rather than have a human laboriously derive a model from a lot of thought.</tt>

I figured they would either use the quote I gave them, paraphrase it, or drop it completely if it didn't fit with the point of the story. But when Chris Anderson's story [_The End of Theory: The Data Deluge Makes the Scientific Method Obsolete_](http://www.wired.com/science/discoveries/magazine/16-07/pb_theory) came out in June 2008, there was a fourth possibility that I hadn't even counted upon: they attributed to me a made-up quote that actually contradicts the reply I gave them:

> _Peter Norvig, Google's research director, offered an update to George Box's maxim: "All models are wrong, and increasingly you can succeed without them."_

To set the record straight: **That's a silly statement, I didn't say it, and I disagree with it.**

The ironic thing is that even the article's author, Chris Anderson, doesn't believe the idea. I saw him later that summer at Google and asked him about the article, and he said "I was going for a reaction." That is, he was being provocative, presenting a caricature of an idea, even though he knew the idea was not really true. That's a mode I expect from [other](http://weeklyworldnews.com/) [publications](http://www.dccomics.com/mad/), but it's not what I want from _Wired_, and I don't expect _Wired_ to make up facts to support their caricature.

Anderson deserves credit for spotting an important development and bringing it to the attention of a wider audience. When he writes "in the era of big data, more isn't just more. More is different.", he has got it just right, in my opinion. But he could have written an article that preserves his key insight while being both provocative _and_ true. He correctly noted that the methodology for science is evolving; he cites examples like shotgun sequencing of DNA. Having more data, and more ways to process it, means that we can develop different kinds of theories and models. But that does not mean we throw out the scientific method. It is not "The End of Theory." It it is an important change (or addition) in the methodology and set of tools that are used by science, and perhaps a change in our stereotype of scientific discovery. Today we think of a scientific breakthrough as the brilliant lone scientist, watching an apple drop or sitting in his bathtub, and suddenly having a _Eureka!_ moment.

In reality, most discoveries are the result of a series of small steps made by many scientists. In the end, the time is right for someone to synthesize these small steps into a new theory. When the new theory is as pithy as _F = m a_, the promoter of the final step can take the lion's share of the credit (even if he points out that he was standing on the shoulders of giants). But if the final step is a complex theory that is not fully known even to the discoverer, but can be approximated by a model derived from massive amounts of data, then things becomes messier--how much of the credit goes to the one who took the final step? How much to the many people who collected the data? How much to the statisticians who helped tune the data models?

Using data and statistics is not a new idea in science, and it is _always_ done with respect to a theory. To take a simple example, if you flip a coin 1000 times and it comes up heads 513 times, you could say that you have a model that predicts a 51.3% (or you might say "about 50%") chance that the next flip will be heads. But that prediction depends on theory: the theory that the future will be similar to the past; the theory that the result of the coin flip does not depend on the current exchange rate for gold, nor on whether there are a prime number of people whose middle name is "Alice" in the room, and so on.

In my talk at ETech, all the examples I gave of using data also involved building models based on a theory. For example, you can create a [spell corrector](spell-correct.html) from data rather than by the sweat and tears of linguists, but you need a model. The current dominant model assumes that words can be modeled by a Markov sequence, that the distribution of words is stationary over time, and that spelling errors with a small edit distance are more likely than errors with a large edit distance. And so on. We recognize that these models leave out a lot of phenomena, but they are good enough for the task at hand.

I think we are all agreed that models are here to stay, and that it doesn't make sense to talk of doing science (or computer science) without them. There is an important technical point about the use of data for large-scale non-parametric models that I would characterize thusly:

> In complex, messy domains, particularly game-theoretic domains involving unpredictable agents such as human beings, there are no general theories that can be expressed in simple equations like _F = m a_ or _E = m c_<sup>2</sup>. But if you have a dense distribution of data points, it may be appropriate to employ non-parametric density approximation models such as nearest-neighbors or kernel methods rather than parametric models such as low-dimensional linear regression.

But perhaps only a statistician could love that idea. I care deeply about how to adapt methods like support vector machines to very large data sets in a computationally tractable way. But I understand that the casual reader of _Wired_ might not share that passion.

However, there is another point that should appeal to all: the idea that it can be difficult to fully understand the implications of a complex model. I think that should have been the centerpiece of Anderson's article (and then he could have quoted me accurately). The great thing about _F = m a_ is that it is so simple that we can easily see how to apply it to falling objects on Earth, and then to the orbits of the moon and planets, and then to the flight of spacecraft. But complex models may hold secrets that they are less willing to give up.

There's a famous (well famous in Artificial Intelligence circles, anyways) Zen koan that goes like this:

> In the days when Sussman was a novice, Minsky once came to him as he sat hacking at the PDP-6.  
> "What are you doing?", asked Minsky.  
> "I am training a randomly wired neural net to play Tic-Tac-Toe," Sussman replied.  
> "Why is the net wired randomly?", asked Minsky.  
> "I do not want it to have any preconceptions of how to play", Sussman said.  
> Minsky shut his eyes.  
> "Why do you close your eyes?", Sussman asked his teacher.  
> "So that the room will be empty."  
> At that moment, Sussman was enlightened.

Minsky was showing Sussman that the randomly-wired neural net (a complex model if ever there was one) actually _did_ have preconceptions; it's just that we don't understand what these preconceptions are. So it is with large data sets. There is plenty to learn from them, both about the domains that the data come from, and about the methodology for learning from data.

But to be clear: the methodology still involves models. Theory has not ended, it is expanding into new forms. Sure, we all love succinct theories like _F = m a_. But social science domains and even biology appear to be inherently more complex than physics. Let's stop expecting to find a simple theory, and instead embrace complexity, and use as much data as well as we can to help define (or estimate) the complex models we need for these complex domains.

OK, so _Wired_ had an important insight, but missed the real story, and misquoted me. At the time I was willing to shrug off the misquote. But the _New Yorker_ article inspired me to aspire higher. Publications can and should have a higher standard for accuracy, and we readers should call them on it when they miss.

So, three cheers for [John McPhee](http://www.johnmcphee.com/), for [_The New Yorker_](http://newyorker.com), and for their [corps of fact-checkers](http://www.newyorker.com/reporting/2009/02/09/090209fa_fact_mcphee). I'm proud that my subscription to _The New Yorker_ supports the fact-checkers in some small way.

As for _Wired_, I have one closing thought: _All we want are the facts, ma'am._

* * *

[Peter Norvig](/)

* * *
