---
layout: post
title:  "Online IDE"
date:   2015-09-22 12:00:00
categories: Test Post
comments: true
---


https://codeanywhere.com/

####Which is better, coding using an online IDE or a standard offline IDE?


https://www.quora.com/Which-is-better-coding-using-an-online-IDE-or-a-standard-offline-IDE

For those with a reasonable home or office internet connection an online IDE can be as responsive as your local IDE.  But you should consider the sum of your developer toolset, not just the IDE - for most developers working on larger projects there is a lot of wasted time and resources spent configuring and maintaining the developer edit, build, run and debug environments.  Add to this the waiting for large builds to complete on your local machine and for your project's infrastructure to start each time you want to run/debug and there can be a lot more wasted time in your day than you'll see in any small latency with a cloud editor.

Certainly, local IDEs have more features but as cloud IDEs catch up (and they are), expect that increasingly the differences will be minimal and related to edge cases. 

By contrast, cloud IDEs have a growing advantage because they can provide developers true parallel edit/build/debug/run and near infinite resources for larger, more complex projects.  As our industry moves to microservices, APIs, OSS and containers, I expect projects to grow more complex in their dependencies and the benefits of cloud development solutions to become more and more obvious.



Its hard to say which is better per say, certainly the Desktop has a lot going for it and it is still the standard. But on the other hand the Cloud IDE has features that a Desktop just cant compare to, for example here are some advantages of the Cloud IDE:

   a. No Setup 
   b. No Configuration 
   c. No Administration 
   d. Access from anywhere 
   e. The ability to Share resources 
   f. Collaboration 
   g. No Hardware Limitations (i.e. the size of a DB being lager than your local storage
  e. Automatically Backups
  
  
Definitely a local IDE. I've tried to use an online IDE but it's inconvenient and performance suffers. Things really start to slow down as you continue coding. 

If you're asking because of a concern over  cloud storage, try installing Dropbox on your machine and save your code that way; editing using an IDE. You get native performance with the redundancy of cloud storage.

So far I prefer a local IDE if all the resources are local. For larger code bases and when doing refactoring, the UI latency tends to be significant to cause inconvenience.


####How is code executed in the browser

https://www.quora.com/How-do-online-IDEs-compile-and-display-results-of-a-code-written-in-the-online-code-editor

The key here is that the code is not executed in the browser.

The code is sent over to their server (maybe in a Ajax request). The appropriate language runtime runs the code on the server and produces the output.

The output is then sent back to the client and gets displayed in the browser.


https://codenvy.com/resources