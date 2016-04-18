---
layout: post
title:  "Belief & Evidence in Empirical Software Engineering"
date:   2016-03-25 10:00:00
categories: Review
comments: true
author: Rahul Pandita
---

In this paper authors comment on how beliefs of software developers (within Microsoft) vary and how they are primarily formed by the personal experiences. Authors also comment on why software engineering researchers should strive to present their findings by relating them to existing beliefs of developers to encourage further adoption of research into practice.

[Article link](http://macbeth.cs.ucdavis.edu/belief+evidence.pdf)


### Abstract

>Empirical software engineering has produced a steady stream of evidence-based results concerning the factors that affect important outcomes such as cost, quality, and interval. However, programmers often also have strongly-held a priori opinions about these issues. These opinions are important, since developers are highly trained professionals whose beliefs would doubtless affect their practice. As in evidence-based medicine, disseminating empirical findings to developers is a key step in ensuring that the findings impact practice. In this paper, we describe a case study, on the prior beliefs of developers at Microsoft, and the relationship of these beliefs to actual empirical data on the projects in which these developers work. Our findings are that a) programmers do indeed have very strong beliefs on certain topics b) their beliefs are primarily formed based on personal experience, rather than on findings in empirical research and c) beliefs can vary with each project, but do not necessarily correspond with actual evidence in that project. Our findings suggest that more effort should be taken to disseminate empirical findings to developers and that more in-depth study the interplay of belief and evidence in software practice is needed.

---


### Thoughts


Authors present their design decisions and lessons learned with the program analysis platform Tricorder.

##### TRICORDER ARCHITECTURE 



#### Statements provided

* Code quality (defect occurrence) depends on which programming language is used.
* Fixing defects is riskier (more likely to cause future defects) than adding new features.
* Geographically distributed teams produce code whose quality (defect occurrence) is just as good as teams that are not geographically distributed.
* When it comes to producing code with fewer defects specific experience in the project matters more than overall general experience in programming.
* Well commented code has fewer defects
* Code written in a language with static typing (e.g., C#) tends to have fewer bugs than code written in a language with dynamic typing (e.g., Python)
* Stronger code ownership (i.e, fewer people owning a module or file) leads to better software quality
* Merge commits are buggier than other commits
* Components with more unit tests have fewer customer-found defects
* More experienced programmers produce code with fewer defects
* More defects are found in more complex code
* Factors affecting code quality (defect occurrence) vary from project to project
* Using asserts improves code quality (reduces defect occurrence)
* The use of static analysis tools improves end user quality (fewer defects are found by users)
* Coding standards help improve software quality
* Code reviews improve software quality (reduces defect occurrence)

##### GOOGLE PHILOSOPHY ON PROGRAM ANALYSIS





##### CLOSING NOTES


The publication that came from this work is overall an informative one that makes contributions to both the research and technical communities.
Besides the fact that the paper is well written (which I should note, should unfortunately good writing is harder to come by now a days), there are a few others reasons why we believe this paper got accepted:

1. The design guidelines for Tricorder are strong; again, some are not supported by existing literature. But there is support for each design decision made.
2. There are design decisions at all (guidelines that can be replicated are always good).
3. The project spans years of work with lots of data.
4. It's Google!
5. It's a relevant topic that people care about (and developers can relate to) in research and industry.


Overall, well done Google! :smile:

>  I'm finding that my own "a priori" beliefs are making this harder to read through than it should be!

> Very interesting paper.  When I read the distributed-development-software quality  study, I was completely surprised by the finding that distributed development didn't lower software quality.  There's a lot that gets dropped in person-to-person communications online vs. in-person and it seems like that should matter, but, apparently, there are ways to organize so it doesn't matter.