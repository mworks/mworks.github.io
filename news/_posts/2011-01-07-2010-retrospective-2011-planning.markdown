---
layout: post
title: Looking back on 2010, forward to 2011
author: cstawarz
---


Now that 2010 is over (and I've just completed my first year of working on MWorks), we thought it'd be a good time to review what we accomplished in 2010 and where we're headed in 2011.


### 2010 Highlights ###

To start, here are the highlights of our achievements from the past year:

* Completed the move to [GitHub](https://github.com/mworks-project) for source hosting
* Set up a new [support site](https://mworks.tenderapp.com/)
* Revived the core and client plugins maintained by the DiCarlo lab
* Revived and revamped the nightly build and test regimen
* Released [MWorks 0.4.4]({% post_url news/2010-05-28-0.4.4-released %})
* Greatly improved the performance of dynamic stimuli (movies, drifting gratings)
* Developed two new plugins (dynamics random dots, white noise background)
* Handled 61 [support cases](https://mworks.tenderapp.com/discussions)
* Resolved 44 [issues](http://mworks.lighthouseapp.com/tickets?q=state%3Aresolved&filter=)


### 2011 Planning ###

Looking ahead, along with continued maintenance and general development, we have several major goals for 2011.  Here's a quick overview of those goals, along with *very* rough estimates of when they'll be completed:

* Improve the MWorks documentation and provide a solid set of basic examples to help new users get started quickly

  (Timeline: transfer contents of [old wiki](https://wikis.mit.edu/confluence/display/MWorks/Home) to [Tender](https://mworks.tenderapp.com/) by the end of January; have basic examples done by the end of February)

* Write a new USB HID plugin, which supports both gamepad and keyboard input

  (Timeline: new plugin available for testing by mid February)

* Make plugin development easier

  (Timeline: simplify/improve plugin and component API by end of March)

* Improve the MWorks user experience, particularly the process of creating and modifying experiments

  (Timeline: ongoing; working prototype of non-XML experiment format by end of April?)

* Overhaul automated testing process

  (Timeline: ongoing; major infrastructure changes completed by June?)


### Future releases ###

Finally, I'd like to note that we anticipate making some changes to how we handle MWorks releases in the coming year.  In addition to periodic "blessed" releases (e.g. 0.4.4), we plan to begin putting more emphasis on rolling, incremental releases.  This stems from the observation that the nightly build is already the go-to release for most new users (and all users who want to take advantage of recent enhancements and fixes without waiting for the next official release).  By producing regular builds that are more release-like (mainly by subjecting them to a wider array of automated tests and assigning them distinct version numbers, e.g. 0.4.5.dev-20110107), we hope to allow more people to use the "latest and greatest" code with confidence.

If you'd like to share your thoughts about the release process (or any other aspect of MWorks development), please don't hesitate to [start a discussion](https://mworks.tenderapp.com/discussion/new).
