---
layout: post
title: "Tool dilemma"
date: 2015-02-22 21:49:29 +0100
comments: true
categories: 
---
If you write enterprise-size software in Java, you ran sooner or later into
a dilemma regarding tools.

On one hand you know that using IDEs like Eclipse drives efficiency and adds
support for streamlined workflows. IDEs provide handy features like call
hierarchy and integrated debugging.

On the other hand IDEs tend to introduce questionable artefacts into the
overall build infrastructure, and sometimes lead decisions for questions 
regarding architecture.

If you e.g. use maven as your dependency and build infrastructure then those
IDEs have to completely understand your maven declarations to know about the
classpath, output folders, compiler level etc. You tend to avoid maven features
that your favorite IDE does not understand.

If you always follow standard solutions and best practises, there might be no
big issue between IDE and maven build. But sooner or later there will appear
challenges for the IDE such as cross compiling, multi-projects, generated code.

In such situations it is recommended to take a step back and analyze the
overall requirements for architecture and build infrastructure. 
Why do we have this generated code, where is it used, what does the generation
depend on, when should it executed? 
As a result, you should have created a reasonable model of all build steps and
an acyclic module dependency model.
Often the root of all evil lies in unmanaged architecture and build
infrastructure. Fix this and go ahead.

Step number two should reflect the findings from step one into the actual 
dependency declarations and build infrastructure. A valid result of this
step is a working command line build.

And then it is the last step that the IDE is tweaked to support the desired
architecture. Sometimes, during this step, build infrastructure needs to be
extended or even changed a little bit, but never should the changes go so far
as to change the desired architecture. If the IDE is not able to cover the 
target architecture then you should propable rethink if this IDE is a good 
choice or if your requirements are too ambitious.

