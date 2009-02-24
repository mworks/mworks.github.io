---
layout: default
title: The MonkeyWorks Project
---

## Welcome ##
Welcome to the website for the project page for the MonkeyWorks Application Suite, hosted on <a href="http://github.com">GitHub</a>.


##Frequently asked questions##
### What is MonkeyWorks? ###
MonkeyWorks is a suite of applications and libraries for designing and running realtime experiments, particularly in the domains of psychology and neurophysiology.  It provides high-level tools for specifying an experimental flow (e.g. hierarchical constructs such as "blocks" and "trials", as well as finite state machine constructs such as "states" and transition logic).  In addition, it enables fine control over a wide range of input and output devices, such as monitors, data acquisition systems, and general purpose IO (GPIO) devices.  It was originally created for doing visual neurophysiology experiments, but was designed with flexibility and extensibility in mind.


### Is MonkeyWorks Finished? Can I use it? ###
You can download MonkeyWorks, but do so at your own risk.  MonkeyWorks is an open source project at a _very early stage of development_.  The creators make no warranty whatsoever for this software, and make no guarantees that the software won't ruin your computer, insult your mother, or write nasty _Nature_ News and Views articles about you behind your back.  You should make no assumptions that any part of MW actually works, and if you do decide to use it, you should test your experiments thoroughly to ensure that they actually work the way you expect them to. *We are not responsible.*

It is also important to note that while we're generally willing to be helpful, we can't be in the business of providing support for anyone who downloads software off of this site.  Bottom line: unless someone has explicitly told you that they would help support you, you should consider yourself on your own.

### Assuming that I've read the above warning, how do I get started? ###

*If you want to try using MW*: You can download a nightly (bleeding edge) installer or named release (e.g. "0.43") under the releases tab on the right.
*If you want to browse the code*: checkout our pages on [github](http://github.com/monkeyworks-project).  GitHub makes it very easy to browse through code, without incurring the hassle of a full checkout. 
*If you are interested in seriously playing with the MW code base*: the place to start is the [mw_build repository](http://github.com/monkeyworks-project/mw_build/tree/master). There, you'll find instructions on how to automatically checkout the project in its entirety, along with some guidance on how to build everything.

### How can I help improve MonkeyWorks? ###
Right now, if you're using MW, the most helpful thing you can do is to [report bugs](http://monkeyworks.lighthouse.com) as you find them (see also the "Issue Tracking" sidebar to the right).  The key to productively reporting issues is to provide as much info as possible (e.g. what where you doing when a crash happened, or what experiment caused the crash).  If you really want to be helpful, doing a bit of detective work and coming up with the minimal experiment that exposes a problem will result in the bug being fixed much faster.

If you want to add to fix a bug yourself, the best thing to do is to [fork](http://railsontherun.com/2008/3/3/how-to-use-github-and-submit-a-patch) the relevant project, fix the bug, and then initiate a "pull request" on the github site.  

Another important way that you can extend MW functionality without mucking with the core functionality is to make a plugin.  Example plugins can be found [here](http://github.com/monkeyworks-project/mw_core_plugins).