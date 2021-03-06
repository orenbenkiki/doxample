doxample
========

Example of integrating Doxygen and Automake

This package shows how doxygen can be invoked from within Autoconf and
Automake. There is probably some official way to integrate additional
functionality into the autotools distribution, but the documentation is silent
on this and a quick glance throgh it wasn't encouraging. Hence this uses the
aclocal.m4/acinclude.m4 mechanism instead. It would be great if someone who is
more versed with the internals of autotools would perform better integration
with it.

What this does is add a few flags to the ./configure script (just run
./configure --help to see the list). Most doxygen output format are supported,
additional ones should be easy to support. Documentation is generated in a
'doc' directory.

You can install this package to see how the man pages installation works. The
program installed - doxample - is just a simple "Hello, world!" program. Note
that the doxygen-generated man pages are pretty bad. I usually patch them
heavily using a post-processing script before I install them. This can be added
manually to the Makefile. You might also simply ignore the man pages and just
stick with HTML/PDF/RTF.
