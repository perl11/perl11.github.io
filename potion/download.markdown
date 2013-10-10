---
layout: default
title: Download Potion
---

Binary and src packages are available for linux x86-64, linux i686, darwin (x86-64 12.5.0) and win32 (w64-mingw32) at the [github releases](http://github.com/perl11/potion/releases) page.

Or you can download the latest potion source from [here](http://github.com/perl11/potion).

    $ git clone https://github.com/perl11/potion.git
    $ cd potion

After unpacking potion, cd to that directory and run GNU make:

    $ gmake

There should be no errors and you should see a welcome message at the end of the output with a decent new compiler (clang strongly preferred). See INSTALL.md

If anything goes wrong, you might want to report it [here](http://github.com/perl11/potion/issues).
Note that we don't support strict C++ compilers, MSVC, and BSD make out of the box.


You now have a 'potion' binary in the bin directory. Optionally, to test it, run:

    $ gmake test

## ~

    $ bin/potion the_file_to_run.pn

You can install it globally with

    $ gmake install

## Packaging

For the current architecture run

    $ make dist

to create packages in the 'pkg' directory.

For the various cross-compilers run

    $ tools/mk-release.sh
