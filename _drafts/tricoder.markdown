---
layout: post
title:  "Tricorder: Building a Program Analysis Ecosystem"
date:   2015-09-23 8:00:00
categories: Review
comments: true
author: Rahul Pandita & Brittney Johnson
---

In this paper, authors provide an overview of the program analysis platform "Tricorder" that is being currently used in [Google](https://www.google.com/) for program analysis. They also present a set of guiding principles that went into creating the platform.

[Article link](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43322.pdf)


###Abstract

>Static analysis tools help developers find bugs, improve code readability, and ensure consistent style across a project. However, these tools can be difficult to smoothly integrate with each other and into the developer workflow, particularly when scaling to large codebases. We present TRICORDER, a program analysis platform aimed at building a data-driven ecosystem around program analysis. We present a set of guiding principles for our program analysis tools and a scalable architecture for an analysis platform implementing these principles. We include an empirical, in-situ evaluation of the tool as it is used by developers across Google that shows the usefulness and impact of the platform

---


###Thoughts


Authors present their design decisions and lessons learned with the program analysis platform Tricorder.

#####TRICORDER ARCHITECTURE 

The Tricorder platform accepts as input the code to be analysed and outputs inline comments the code. 
The platform is a realized as a microservice architecture.
Authors argue that thinking in terms of services encourages scalability, modularity, and resilience (in case of node failure).
Tricorder is designed to such that the analysis workers are designed to be replicated and stateless in order to make the system robust and scalable.
The results appear in the code review as comments (Google terms it as *robot comments* or *robocomments* for short).




#####GOOGLE PHILOSOPHY ON PROGRAM ANALYSIS

1. **No false positives**
	"No" may be an over statement as admitted by the authors.
	The aim is to reduce the number of false positives to the minimum.
	Authors also define a *effective false-positives* as a measure of number of reports that a user chose not to take any action.
2. **Empower users to contribute**
	The insight is to leverage the knowledge of masses to build a robust system.
	Google actively encourages users of Tricorder platform to write new analyzers.
	Since the users (google employees) typically work with variety of programming languages and custom APIs, authors seek to leverage the vast domain knowledge of the users to write analysers.
	The "Tricorder" platforms enforces quality by reserving the right to remove an analyser from the system based on performance (i.e. how many users are ignoring warnings, are the warnings annoying, is the analyzer taking too many resources...).
	Authors argue that analyzer writers typically take pride in their work, thus the analyzers are generally of high quality.
	The issues reported against the analyzers are typically resolved fairly quickly.
3. **Make data-driven usability improvements**
	The idea is to avoid arbitrary design and implementation decisions and ground them on empirical evidence.
	Enhancement and correction to analyzers are made based on the user feedback.
4. **Workflow integration is key**
	The key idea is that the analysis should integrate with the users workflow rather than a user having to go out of way to perform analysis.
	For instance, a standalone analyser is less likely to be invoked by a developers in contrast to an analysis mechanism that integrates to his/her IDE.
5. **Project customization, not user customization** 
	`Past experiences at Google showed that allowing user specific customization caused discrepancies within and across teams, and resulted in declining usage of tools.`
	Authors observed that oftentimes when a developer using a tool abandons project, team members often check in code containing warnings found by that tool.
	However, Tricorder platfrom offers limited project-based customization. 
	For instance, a team may choose to run optional analysis by default and some analysis that are not applicable can be disabled for a team.

#####EVALUATION	


blah! blah! **BLAH**

#####CLOSING NOTES


*Reasons why this paper got accepted.*

---

Guest Writer : [Brittney Johnson](http://www4.ncsu.edu/~bijohnso/) is a PhD. at the [Department of Computer Science, NCSU](https://www.csc.ncsu.edu/) focussing on software engineering research. She is the member of [Developer Liberation Front](http://research.csc.ncsu.edu/dlf/) directed by [Dr. Emerson Murphy-Hill](https://people.engr.ncsu.edu/ermurph3/index.html).  
