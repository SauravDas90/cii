Below are the Subversion log entries summarizing the changes in version 2.0.
For changes in versions before 1.2, click [here](http://cii.googlecode.com/svn/tags/v12/history.html).

For the technical details about the interface change in Fmt, see InterfaceChanges2.

```
------------------------------------------------------------------------
r191 | drhanson | 2008-09-08 17:09:51 -0700 (Mon, 08 Sep 2008) | 5 lines
Changed paths:
   M /branches/drh/x86_64/examples/integer.c
   M /branches/drh/x86_64/examples/integer.h
   M /branches/drh/x86_64/examples/sort.c
   M /branches/drh/x86_64/include/ap.h
   M /branches/drh/x86_64/include/fmt.h
   M /branches/drh/x86_64/include/mp.h
   M /branches/drh/x86_64/include/str.h
   M /branches/drh/x86_64/include/text.h
   M /branches/drh/x86_64/src/ap.c
   M /branches/drh/x86_64/src/fmt.c
   M /branches/drh/x86_64/src/mp.c
   M /branches/drh/x86_64/src/str.c
   M /branches/drh/x86_64/src/text.c

Box va_list values in a structure so that the address
of these structures can be passed to format-specific
functions on machine for which a va_list is not a
pointer type, e.g., x86_64 where va_list is a struct.

------------------------------------------------------------------------
r197 | drhanson | 2008-09-27 14:59:31 -0700 (Sat, 27 Sep 2008) | 1 line
Changed paths:
   M /trunk/examples/integer.c
   M /trunk/examples/integer.h
   M /trunk/examples/sort.c
   M /trunk/include/ap.h
   M /trunk/include/fmt.h
   M /trunk/include/mp.h
   M /trunk/include/str.h
   M /trunk/include/text.h
   M /trunk/src/ap.c
   M /trunk/src/fmt.c
   M /trunk/src/mp.c
   M /trunk/src/str.c
   M /trunk/src/text.c

Merge branches/drh/x86_64@191 into trunk.

------------------------------------------------------------------------
r205 | drhanson | 2008-09-28 16:17:13 -0700 (Sun, 28 Sep 2008) | 1 line
Changed paths:
   M /trunk/misc/maxalign.c

Call malloc in misc/maxalign.c to verify MAXALIGN value.

------------------------------------------------------------------------
r207 | drhanson | 2008-09-29 21:43:42 -0700 (Mon, 29 Sep 2008) | 3 lines
Changed paths:
   M /trunk/install.html
   M /trunk/makefile
   M /trunk/misc/maxalign.c

Simplify malloc use in maxalign.c; add maxalign targets in makefile;
update installation guide for X86 Linux and Mac platforms and for
changes in maxalign.c.
```