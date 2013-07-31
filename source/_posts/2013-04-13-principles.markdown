---
layout: post
comments: true
categories: Development, Processes
date: 2013/04/13 02:21:00
title: Development principles I am convinced of
---
In my current company we had tried out several agile processes including Kanban and Scrum, 
but in some areas we have decided to go back to "old school" practises. We have four week iterations, 
continous integration, automated build systems etc. But on the other hand we "push" tasks to 
developers, have code ownership, do very little pair programming and skip to write unit tests in non 
trivial areas like UI. We are successful with this process, but it depends how you measure success.

There are some things I do not like:

* Big back logs, including lot's of prio 4 or 5 bugs you keep to fix them later if you have the time.

* Big stocks of unfinished work, like features in branches that cannot be merged because of x, y, z.

* Requirements on estimations that go beyond a gut feeling. Especially I hate a) to "break down" 
a piece of work, estimate the parts and sum it up, and b) handle estimations like promises. 

* Making detailed plans that go beyond the next week. I have no problems with making plans 
that define a complete year, but the granularity should be appropriate.

And, there are some practises I am convinced of:

* Stick to quality. If a bug appears: fix it or kill it if it is not worth it. If you see stuff to clean up: clean it up.

* Spend time on infrastructure to automate stuff, spend time on improving performance of your 
build process. Use command line scripts to automate stupid, repetitive work.

* Write unit tests that really test a unit of work, i.e. a class. Write unit tests. Do not mistake 
integration tests for unit tests.

* Don't trust process evangelists, every group of people working together in a project needs a 
different process to get the best ressults out. And that process needs to be refactored like your code. 

