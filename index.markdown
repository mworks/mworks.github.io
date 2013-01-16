---
layout: default
title: The MWorks Project
---

## What is MWorks? ##

MWorks is a suite of [open source](http://opensource.org/) applications and libraries for designing and running realtime experiments, particularly in the domains of psychology and neurophysiology.

It provides high-level tools for specifying experimental flow (e.g. hierarchical constructs such as "blocks" and "trials", as well as finite state machine constructs such as "states" and transition logic).  In addition, it enables fine control over a wide range of input and output devices, such as monitors, data acquisition systems, and general purpose I/O (GPIO) devices.

MWorks was originally created for conducting visual neurophysiology experiments, but it was designed with flexibility and extensibility in mind.

## Is MWorks finished? Can I use it? ##

Currently, MWorks is in production use in labs at [MIT](http://mit.edu/), [Harvard](http://www.harvard.edu/), the [University of Pennsylvania](http://www.upenn.edu/), the [German Primate Center](http://www.dpz.eu/en/home.html), and the [International School for Advanced Studies (SISSA)](http://www.sissa.it/).  Our user base is growing continually, and we encourage potential users to check out our [knowledge base](http://help.mworks-project.org/kb) and [contact us](http://help.mworks-project.org/discussion/new) with any questions.

That said, if you choose to download and use MWorks, be aware that you do so *at your own risk*.  The developers make no guarantee that MWorks is suitable for your purposes or that it will work as advertised (for details, see the [software license](https://raw.github.com/mworks/mworks/master/LICENSE.txt)).  If you decide to use it, you should test your experiments thoroughly to ensure that they actually work as you expect.  *We are not responsible.*

Also, while we'd like to support as many users as possible, please be aware that our resources are limited.  Most of the labs currently using MWorks make significant contributions to its development, either by helping to maintain and improve the source code or by providing financial support to the development team.  If you use MWorks in your research and need ongoing support, we may ask you to contribute, too.

## How do I get started? ##

__If you want to try using MWorks:__ Read the [installation guide](http://help.mworks-project.org/kb/installation/installing-mworks) to learn how to download and install the software.

__If you want to browse the code:__ Check out [our pages](https://github.com/mworks) on [GitHub](https://github.com/).  GitHub makes it very easy to browse through code without incurring the hassle of a full checkout. 

__If you're interested in seriously playing with the MWorks code base:__ You'll probably need some help to get started.  Please [contact support](http://help.mworks-project.org/discussion/new), and we'll get you going.

## How can I help improve MWorks? ##

If you're using MWorks, the most helpful thing you can do is to [report bugs](http://help.mworks-project.org/discussion/new) as you find them.  The key to reporting issues productively is to provide as much information as possible (e.g. what you were doing when a crash happened, or what experiment caused the crash).  If you really want to be helpful, doing a bit of detective work and coming up with a minimal experiment that exposes the problem will result in the bug being fixed much faster.

If you want to add to MWorks or fix a bug yourself, the best thing to do is to [fork](https://help.github.com/articles/fork-a-repo) the main [MWorks repository](https://github.com/mworks/mworks), fix the bug, and then initiate a [pull request](https://help.github.com/articles/using-pull-requests).

Another important way that you can extend MWorks' functionality without modifying the core libraries is to create a plugin.  If you're interested in doing this, a good way to start is by checking out some [example plugins](https://github.com/mworks/mworks/tree/master/plugins/core).
