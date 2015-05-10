Below are the Subversion log entries summarizing the changes in version 1.2.
For changes in previous versions, click [here](http://cii.googlecode.com/svn/tags/v12/history.html).

```
------------------------------------------------------------------------
r183 | drhanson | 2007-06-14 06:39:57 -0700 (Thu, 14 Jun 2007) | 2 lines
Changed paths:
   M /trunk/src/thread.c

Simplify stack alignment code; shorten interrupt interval.
------------------------------------------------------------------------
r182 | drhanson | 2007-06-13 23:45:26 -0700 (Wed, 13 Jun 2007) | 4 lines
Changed paths:
   M /trunk/install.html
   M /trunk/makefile

Revise makefile so BUILDDIR includes the trailing slash,
which makes it possible to build in the current directory when BUILDDIR is undefined.
Update install.html accordingly, and add Mac OS X to Linux make command.
------------------------------------------------------------------------
r181 | drhanson | 2007-06-13 23:26:23 -0700 (Wed, 13 Jun 2007) | 3 lines
Changed paths:
   M /trunk/makefile
   M /trunk/src/swtch.s
   M /trunk/src/thread.c

Add Intel Mac OS X, which requires that the stack is aligned on
16-byte boundaries at calls. Fix 16-byte alignment botch. Some cosmetics.
------------------------------------------------------------------------
r178 | drhanson | 2007-05-31 13:56:55 -0700 (Thu, 31 May 2007) | 1 line
Changed paths:
   D /trunk/solaris.mk

Delete Solaris dreg.
------------------------------------------------------------------------
r174 | drhanson | 2007-05-28 09:17:35 -0700 (Mon, 28 May 2007) | 1 line
Changed paths:
   A /trunk/misc
   A /trunk/misc/maxalign.c

Add maxalign.c.
```