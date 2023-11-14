# libstree a library for suffix trees
This is a fork of the libstree library http://www.icir.org/christian/libstree/ by Christian Kreibich.
The primary purpose of this form is to provide a permanent location for this small, performant implementation
of suffix trees and ensure its perl API continues to work https://metacpan.org/pod/Tree::Suffix .

The following is taken verbatim from the original README file in the libstree library. 


                     L   I   B   S   T   R   E   E


     A generic library for string algorithms based on suffix trees

              http://www.cl.cam.ac.uk/~cpk25/libstree/
          Christian Kreibich <christian.kreibich AT cl.cam.ac.uk>

------------------------------------------------------------------------

LibSTree is a library containing generic versions of string algorithms
based on suffix trees. The underlying implementation is based on
Ukkonen's linear suffix tree creation algorithm, supporting multiple
strings per tree.

It is generic in that the string items can be arbitrary structures,
e.g. normal character strings, binary strings, complex objects etc.
String item functionality is virtualized through replaceable function
pointers.

Other things that make LibSTree look good:

- It provides a function that *removes* a previously inserted string
from a tree. The resulting tree looks exactly as if the removed string
had never been inserted. This allows you to iteratively add and remove
strings from a tree which is useful in many cases.

- The longest common substring algorithm returns all longest sub-
strings, at least having a given length if desired, and either up to
a given length limit or with the largest length found. 


The suffix tree implementation closely follows the explanation given
in Dan Gusfield's book named "Algorithms on Strings and Trees",
Cambridge Univ. Press, 1997. Great book. Chances are you want to read
either that or the original paper in order to understand the code.

Given that LibSTree is a self-contained library, it should build on
any major OS out there or at least be easy to port. Reported to work:

- Linux
- OpenBSD


Requirements:
=============

	* none, other than gcc or some other compiler.


Build:
======

To build libstree, check your available build options using

   > ./configure --help

and then build it using

   > ./configure [options]; make; make install


CVS users, you have to create the configure script first. Use the in-
cluded autogen.sh script, which will usually work fine. We try to
support various autoconf/automake combinations, we also support both a
configure.ac and a configure.in template.

There are example programs in the test/ subdirectory, please have a look
at those. 
