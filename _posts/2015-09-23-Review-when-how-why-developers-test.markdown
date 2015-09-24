---
layout: post
title:  "When, How, and Why Developers (Do Not) Test in Their IDEs"
date:   2015-09-23 8:00:00
categories: Review
---


[Article link](http://www.st.ewi.tudelft.nl/~mbeller/publications/2015_beller_gousios_panichella_zaidman_when_how_and_why_developers_do_not_test_in_their_ides.pdf)


####Abstract

>The research community in Software Engineering and Software Testing in particular builds many of its contributions on a set of mutually shared expectations. Despite the fact that they form the basis of many publications as well as open-source and commercial testing applications, these common expectations and beliefs are rarely ever questioned. For example, Frederic Brooks’ statement that testing takes half of the development time seems to have manifested itself within the community since he first made it in the “Mythical Man Month” in 1975. With this paper, we report on the surprising results of a large-scale field study with 416 software engineers whose development activity we closely monitored over the course of five months, resulting in over 13 years of recorded work time in their integrated development environments (IDEs). Our findings question several commonly shared assumptions and beliefs about testing and might be contributing factors to the observed bug proneness of software in practice: the majority of developers in our study does not test; developers rarely run their tests in the IDE; Test-Driven Development (TDD) is not widely practiced; and, last but not least, software developers only spend a quarter of their work time engineering tests, whereas they think they test half of their time.

---

####Thoughts
Authors attempt to address the pressing issues: *"How much should we test? And when should we stop testing?"*  in part, by analyzing the development activities of 416 developers spanning several countries having varied experiences.
They achieve this by having the developers volunteer the development information by installing a [WatchDog](http://testroots.org/testroots_watchdog.html) plugin in their IDE's (currently eclipse and IntelliJ Idea). Authors describe in detail what activities they monitor and explain how they co-relate the activity type with with various activities such as testing, reading code, running tools, or writing production code.

Authors question the age-old accepted statement that developers *spend more than half their time on testing*. 
According to their analysis developers spend 25% of their time in *writing* test classes.
*They equate testing time with the time spent on writing test code. However, there might be cases when developers are refactoring production code as a part of testing*.
Furthermore, authors provide evidence that developers generally over-estimate the time they spend on testing.

They also report that there is lack of conformance with strict TDD even-though the developers claim they are following the TDD practice.
They leverage non-finite-automata (NFA) to detect conformance that may have some limitations. 
*The NFA may have limitations in terms of detecting TDD conformance, thus the exact numbers **may** be off. However, the general lack of adherence to TDD practice is evident.* 

As far as I am concerned, the most interesting aspect of the paper is the statement that developers may rely on the external build systems (build-failures) and continuous integration (CI) systems for maintaining software quality outside of an IDE.
If that is true then the CI systems can be made more intelligent.
For instance, a CI system can monitor developer activity and fire-up the relevant test cases in background.
The results are then made available to developers just-in-time to make changes to the production code.
In short, remove the reliance on the developers to explicitly run tests and simultaneously bring down the response time of the test results (as opposed to test being fired after the developer has explicitly issued request to CI system).

Furthermore, the intelligent CI system could also run analytics to notify developer of the lack test code and automatically come up with test code skeleton for developer to fill in the test logic.
[Microsoft Pex](http://research.microsoft.com/en-us/projects/pex/) has a similar capabilities of comming up with skeleton code for performing automated unit testing in Visual Studio Environment for C#.

PS: Author use various statistical test to evaluate their research questions. These test seems to be relevant in general research setting.