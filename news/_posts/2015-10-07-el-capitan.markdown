---
layout: post
title: MWorks and El Capitan
author: cstawarz
---

Now that [OS X 10.11 (El Capitan)](https://en.wikipedia.org/wiki/OS_X_El_Capitan) is available, here are some things to consider before upgrading your Mac to the new OS.


### MWorks compatibility

Under El Capitan, [MWorks 0.5.1]({% post_url news/2014-05-22-0.5.1-released %}) exhibits serious issues with the stimulus display, which essentially render it unusable.  If you are currently running MWorks 0.5.1 or earlier and are unwilling or unable to upgrade, **do not install El Capitan**.

The stimulus display issues are fixed in [MWorks 0.6]({% post_url news/2015-10-06-0.6-released %}).  If you want to use MWorks on a Mac running El Capitan, you *must* use version 0.6 or later.


### Device driver restrictions

Starting with version 10.10 (Yosemite), OS X requires all [kernel extensions](https://developer.apple.com/library/mac/documentation/Darwin/Conceptual/KernelProgramming/Extend/Extend.html) to be [code signed](https://developer.apple.com/library/mac/documentation/Security/Conceptual/CodeSigningGuide/Introduction/Introduction.html).  Unsigned kernel extensions will not load, and any hardware that depends on those extensions will not function.  This will affect some MWorks users, as the device drivers for the [InstruTECH ITC-18](http://heka.com/products/products_main.html#acq_itc18) and [National Instruments DAQs](http://www.ni.com/data-acquisition/) are *not* code signed, meaning those devices will not function under a standard OS X installation.

If you are running Yosemite or El Capitan and want to use one of these devices, you must first disable the kernel extension code signing requirement.  On Yosemite, this is done by [executing a simple command and restarting](http://apple.stackexchange.com/questions/163059/how-can-i-disable-kext-signing-in-mac-os-x-10-10-yosemite).  On El Capitan, the [process is more complicated](https://developer.apple.com/library/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/ConfiguringSystemIntegrityProtection/ConfiguringSystemIntegrityProtection.html) and requires that you completely disable the new [System Integrity Protection](https://developer.apple.com/library/mac/documentation/Security/Conceptual/System_Integrity_Protection_Guide/Introduction/Introduction.html) feature, meaning your Mac will not benefit from the additional security layers that it provides. 


### General considerations

With any major OS update, it's usually wise to wait a few months (or at least until the first patch release, i.e. 10.11.1) before upgrading any production machines.  This gives the wider Mac user community a chance to shake out any bugs that were missed in pre-release testing, and it gives third-party software vendors some time to upgrade the tools you depend on for the new OS.

Other than the issues discussed above, I have not encountered any problems with running MWorks under El Capitan.  However, given that the new OS was released only a week ago, it's still too early for me to give a confident "all clear".  If you really want to upgrade now (or have just purchased a new Mac that *can't* run an earlier OS), I recommend that you test your experiments and I/O devices thoroughly to ensure that everything works as expected.
