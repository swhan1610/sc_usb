USB library
...........

:Stable release:  unreleased

:Status:  feature complete

:Maintainer:

:Description:  Library to interface with USB2 PHY


Key Features
============

* Source code to deal with common requests of endpoint0
* Source code to deal with multiple endpoints in a single thread using
  interrupts (experimental)
* Example Mouse HID application
* Example combined Mouse/Keyboard HID application
* Example CDC/ECM (Ethernet over USB) application
* Example CDC/PSTN (Virtual COM port) application
* Example CDC/EEM (Ethernet Emulation) application (experimental)

To Do
=====

* Port documentation

* Complete the Interrupt experiment (vcom) by porting endpoint0 to the
  interrupt layer.

Firmware Overview
=================

This module contains the code that deals with the common requests on
endpoint0, and a series of example USB devices that can be built, including
HID, and three CDC devices (Ethernet, Modem). 

Known Issues
============

* The virtual COM port example is experimental and uses interrupts to
  reduce thread-count - this needs more testing to check that the turnaround
  times are reliable.

* Some devices are based on a funky keyboard with two embedded L1s, other
  on the L1-audio board. All should be ported to the L1-audio board so that
  there is a platform on which this code can be ran.

* The EEM example needs testing - it needs a host that supports EEM!

Required Repositories
================

* xcommon git\@github.com:xcore/xcommon.git
* sc_xud git\@github.com:xcore/sc_xud.git
* sc_ps2 git\@github.com:xcore/sc_ps2.git (keyboard+mouse only)

Support
=======

Issues may be submitted via the Issues tab in this github repo. Response to any issues submitted as at the discretion of the maintainer for this line.
