---
layout: post
title: "Determining affected tests using coverage info"
date: 2015-05-01 00:36:32 +0200
comments: true
categories: [test coverage, cobertura, git, maven]
---
If have got an idea inspired by [this post](http://tenderlovemaking.com/2015/02/13/predicting-test-failues.html).

Every time when me or a build server runs a complete build on a commit with all tests, it could store
detailed coverage information and associate it with this commit.

Later on, when for instance I am fixing a bug, it should be possible to git diff the working directory to the latest
parent commit that has associated coverage info. Looking up the changes and the coverage info, one could tell what
tests are likely to be affected by the changes in between.

If I then run only those tests, I am pretty confident that other tests will not break by my changes. I am not 100% sure
but I am confident enough to commit the stuff and let the build server run a complete build which leads to new
coverage info associated with this new commit.

Some requirements I have in mind:

 - Should work as a maven goal "mvn affected:test"
 - Should work with git to provide diff and coverage info association.
 - Should work with remotely stored coverage info. (Is it possible to store custom information associated with a commit into git repository?)
 - Should work with [cobertura](http://mojo.codehaus.org/cobertura-maven-plugin/dump-datafile-mojo.html)

I would really like to know, if I am the only one that thinks such a maven plugin would be useful,
what obstacles you see, if there are better alternatives to cobertura and git or if a broader approach would make more sense.
Let me know.
