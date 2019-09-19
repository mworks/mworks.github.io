---
layout: post
title: End of life for NI-DAQmx Base driver
author: cstawarz
---

National Instruments (NI) [recently announced](https://forums.ni.com/t5/NI-DAQmx-Base-Developers/End-of-Life-Announcement-for-DAQmx-Base-Driver/gpm-p/3967360?profile.language=en) that they are ending development of the NI-DAQmx Base device driver package.  Given that the most recent version of NI-DAQmx Base (15.0) was released four years ago, this news is not especially surprising.  However, it will affect anyone using NI devices with MWorks, as detailed below.


### How this affects MWorks users

MWorks' [NIDAQ device](/documentation/latest/components/nidaq_device.html) uses NI-DAQmx Base to interface with NI hardware.  NI has stated that the current (and final) version of NI-DAQmx Base will not be compatible with macOS Catalina (10.15), which is due to be released some time next month.  Therefore, if you wish to continue using NI devices with MWorks, you will need to be running macOS 10.14 or earlier.

Extrapolating Apple's recent cadence of macOS releases in to the future, we can expect macOS 10.16 to be released in the fall of 2020, with 10.17 following in the fall of 2021.  At that point, Apple will end support for macOS 10.14, and MWorks will follow suit.  Hence, the spring 2022 release of MWorks will require macOS 10.15 or later.  Unless NI changes course and provides an updated or replacement driver package for macOS, MWorks' support for NI devices will end with this release.


### Options for the future

If you currently use NI hardware with MWorks and would like to continue to do so in the future, you may want to get in touch with the folks at NI and lobby for continued support of macOS.  However, assuming that NI is unwilling to change its plans, you need to start considering alternative I/O hardware.

For control and simple data-acquisition tasks, I heartily recommend MWorks' [Firmata interface](/documentation/latest/components/firmata_device.html).  Firmata-compatible devices (e.g. [Arduino](https://www.arduino.cc) boards) are inexpensive, flexible, and ever-increasingly powerful.  They are an excellent choice for controlling juice pumps, monitoring digital or analog triggers, and many other I/O tasks.

If you require more traditional DAQ hardware (for example, you need to record many analog channels simultaneously, or you require a sampling interval of less than one millisecond), I suggest that you consider [LabJack](https://labjack.com) devices.  Several labs currently use the LabJack [U6](https://labjack.com/products/u6) with MWorks (via a custom plugin), and I'm planning to include built-in support for the [T4](https://labjack.com/products/t4) and [T7](https://labjack.com/products/t7) in the next MWorks release.

Finally, if you'd prefer to use I/O hardware from another vendor, please [get in touch](https://mworks.tenderapp.com/discussion/new), and we can discuss options for interfacing with it from MWorks.  In general, we should be able to support any device that comes with a macOS-compatible C/C++ API or communicates with the host computer via a platform-agnostic protocol (e.g. Ethernet or serial).
