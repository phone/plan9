This is a port of many Plan 9 libraries and programs to Unix.

Elliot's Fork
-------------

Most of my changes are related to the functionality of acme(1). In
general, I tremendously enjoy acme's mouse-driven approach to editing,
but for some common tasks, I still prefer keyboard shortcuts. I have
added a number of keyboard commands that I find universally useful:

* `C-t`: move the mouse into the Tag.
* `C-o`: set the `ESC` marker, as though you had clicked. when you
  press `ESC` again, if you haven't clicked somewhere since, dot will
  be set to the text between this marker and your cursor.
* `ENTER`: if have hit `ESC` to highlight some text, and you haven't
  done any other editing since, you can hit `ENTER` within 15 seconds
  to execute dot (the highlighted text).
* `%-R`: Redo. In Russ' p9p, this is a debug command to toggle hidpi
  mode. That toggle is set to `%-0` in my fork.

### To Do / In Progress

* Allow customizeable FKeys. Run e.g `FKey 3 '|a+'` to set `[F3]` to
  run `|a+` whenever it's pressed. I think e.g `FKey 3` with no arg
  would print the current setting.
* On OS X, make and install a proper bundle for Acme -- how to deal
  with args tho? Maybe a separate command to install it?
* Update man page

Installation
------------

To install, run ./INSTALL.  It builds mk and then uses mk to
run the rest of the installation.

For more details, see install(1), at install.txt in this directory
and at https://9fans.github.io/plan9port/man/man1/install.html.

Documentation
-------------

See https://9fans.github.io/plan9port/man/ for more documentation.
(Documentation is also in this tree, but you need to run
a successful install first.  After that, "9 man 1 intro".)

Intro(1) contains a list of man pages that describe new features
or differences from Plan 9.

Helping out
-----------

If you'd like to help out, great!

If you port this code to other architectures, please share your changes
so others can benefit.

Git
---

You can use Git to keep your local copy up-to-date as we make
changes and fix bugs.  See the git(1) man page here ("9 man git")
for details on using Git.

Status
------

[![Build Status](https://travis-ci.org/9fans/plan9port.svg?branch=master)](https://travis-ci.org/9fans/plan9port)
[![Coverity Scan Build Status](https://scan.coverity.com/projects/plan-9-from-user-space/badge.svg)](https://scan.coverity.com/projects/plan-9-from-user-space)


Contact
-------

* Mailing list: https://groups.google.com/group/plan9port-dev
* Issue tracker: https://github.com/9fans/plan9port/issues
* Submitting changes: https://github.com/9fans/plan9port/pulls

* Russ Cox <rsc@swtch.com>
