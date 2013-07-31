---
categories: Development, Processes
layout: post
comments: true
date: 2013/04/18 21:24:00
title: Avoid big bug backlogs
---
I strongly recommend to avoid long lists of bugs. Today, we have cool tools like [Bugzilla](http://bugzilla.org)
or [Jira](http://www.atlassian.com/software/jira/) that make tracking bugs real fun even if there are big numbers of it.

I can imagine a situation where a software product has no known bugs and is complete in a functional sense. 
However, I have never been in this situation since I have started working on software. The typical situation I experience is:

* you have got plenty of things that should be improved, extended, added - more than you can implement.

* you have got plenty of bug tickets, more than you can handle.

If you are in a situation where you sell software you are developing you also have to
weigh effort, priorities, expected damage caused by bugs and expected gain from improvements. You cannot 
implement what you want. So how about filling lists of features, lists of bugs, prioritize them, estimate
them roughly, and finally decide what is the next important item that should be implemented? It sounds
promising. You only have to manage one list that is sorted by a function depending on effort, estimate, 
priority etc. and sort new items into this list.

Feed the first four items of this ultimate list to a [Kanban-Board](http://en.wikipedia.org/wiki/Kanban_board)
every day and let the developers pick items in order.

Bullshit.

In my experience you cannot prioritize bugs and features into one list. You simply cannot compare
them. Maybe a prioritized backlog is good for features, but it is not for bugs. Bugs are not a thing
of planning or betting on. Bugs are the bill you get for your past work. You simply cannot avoid to pay that bill.

I recommend the following to process bugs:

* If a bug comes in: Decide if it is really a bug or possibly an enhancement (enhancement -> feature backlog).

* Decide if you want to fix the bug. The decision should only take into account the level of quality
you want to deliver, not what other things you have on your agenda.

* If the bug is not important enough - and this is the important point - *close it as "won't fix"*. 

* Otherwise choose between three severities: Fix it "now", "today or tomorrow", "within the next two weeks".

* Assign the bug to a person that should fix it actually.

* Measure time spent on bug fixing. If it goes beyond 15 percent take a sharp look what is happening with
your software.

So why not simply give non important bugs a low priority and keep them in the list? Why not say: "Hey,
if one has nothing to do: just pick a bug from the "non-important" pool." For me this would be a statement
like "We provide a quality level that depends on the time that is left over". 
It is also unclear if this sort of bugs should be part of a "open bugs" statistic. More: In the 
unlikely case that someone would have time left over: What bug would she select? How would she choose from
the list of 100k bugs?
So just close these bugs and enjoy the pleasures of the real, lean bug list.  
