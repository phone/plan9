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
and at http://swtch.com/plan9port/man/man1/install.html.

Documentation
-------------

See http://swtch.com/plan9port/man/ for more documentation.
(Documentation is also in this tree, but you need to run
a successful install first.  After that, "9 man 1 intro".)

Intro(1) contains a list of man pages that describe new features
or differences from Plan 9.

Helping out
-----------

If you'd like to help out, great!  The TODO file contains a small list.

If you port this code to other architectures, please share your changes
so others can benefit.

Contact
-------

* Mailing list: http://groups.google.com/group/plan9port-dev
* Issue tracker: http://code.swtch.com/plan9port/issues/
* Submitting changes: http://swtch.com/go/codereview

* Russ Cox <rsc@swtch.com>
