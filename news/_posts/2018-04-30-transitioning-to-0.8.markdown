---
layout: post
title: Transitioning to 0.8
author: cstawarz
---

[MWorks 0.8]({% post_url news/2018-04-27-0.8-released %}) is a large and significant release.  Here are a few notes to aid your transition to the new version.


### MWEL is great, but XML is still fully supported

[MWEL](/documentation/latest/mwel/) has many advantages over traditional MWorks experiment XML, and I recommend it for all new experiments.  However, the availability of MWEL does *not* mean that XML-based experiments are no longer supported.  (In fact, at runtime, MWEL experiments are translated into XML, after which they are parsed and executed in exactly the same way as XML-based experiments.)

If you have working XML-based experiments, there is no need to convert them to MWEL.  They will continue to function as before.


### Default server address

Both MWServer and MWClient now use "localhost" (instead of 127.0.0.1) as the default server address.  If you're having trouble connecting MWClient to MWServer, check that the same host name is used in both applications.  (For details on how to do this, see [Launching the Applications](/documentation/latest/guide/running.html#launching-the-applications) in the user manual.)


### Color management

MWorks' stimulus display now performs [color management](https://en.wikipedia.org/wiki/Color_management).  Specifically, stimuli are rendered in a "linearized" [sRGB color space](https://en.wikipedia.org/wiki/SRGB).  The RGB values in a stimulus' `color` parameter are interpreted as belonging to this color space, and image files are [color matched](https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/csintro/csintro_conversion/csintro_conversion.html#//apple_ref/doc/uid/TP30001148-CH223-SW1) to this color space.  Before being presented, each output frame is converted to the target display's color space.

For more information on why this matters, see [this discussion](https://mworks.tenderapp.com/discussions/suggestions/369#comment_31900668).  Most users probably won't see much of a difference (although the default, 50%-gray background will be noticeably brighter).  However, if these changes prove incompatible with your setup (for example, if you've manually "linearized" your display), color management can be disabled, either directly in [#mainScreenInfo](/documentation/0.8/reference/sysvars.html#mainscreeninfo), or via MWServer's preferences window.


### Stimulus plugins must now use OpenGL 3.3

Prior to version 0.8, MWorks' stimulus drawing code used the (rather ancient) OpenGL 2.1 API.  As part of porting MWorks to iOS, all drawing code has been updated to use the (somewhat less ancient) OpenGL 3.3 Core Profile API, which is largely compatible with the OpenGL ES 3.0 API available on iOS.

If you maintain a custom stimulus plugin, updating it to function with MWorks 0.8 is going to take some work.  Apple has an [overview document](https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/OpenGL-MacProgGuide/UpdatinganApplicationtoSupportOpenGL3/UpdatinganApplicationtoSupportOpenGL3.html) describing the changes required to move from OpenGL 2.1 to 3.3.  However, if your plugin derives from a standard MWorks stimulus, then the best starting point is probably the current [source code](https://github.com/mworks/mworks).

If you have any questions or need assistance in updating your plugin, please [contact us](https://mworks.tenderapp.com/discussion/new).
