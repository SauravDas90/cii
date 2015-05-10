# Introduction #

Subversion [revision 197](https://code.google.com/p/cii/source/detail?r=197) changes the [Fmt](http://cii.googlecode.com/svn/trunk/include/fmt.h) interface,
and this change affects any interface that uses `Fmt_T` or defines a formatting function, e.g., `Str_fmt`.

# Details #

As of C99 (International Standard ISO/IEC 9899), some  stdarg.h implementations, e.g., Linux gcc, forbid
taking the address of a `va_list` or copying a `va_list` by simple assignment.
Versions 1.x of the Fmt interface passed addresses of `va_list` values to
the formatting functions, and thus fail on these implementations.

Passing the address of a `va_list` requires wrapping the `va_list` in structure and passing the address of that structure. Copying a `va_list` requires using the `va_copy` macro.

Fmt now defines

```
typedef struct va_list_box {
	va_list ap;
} va_list_box;
```

and passes `va_list_box*` values to the formatting functions.
Those functions now use the `ap` field, e.g., version 1.2 of `Str_fmt`

```
void Str_fmt(int code, va_list *app,
	int put(int c, void *cl), void *cl,
	unsigned char flags[], int width, int precision) {
	...
	s = va_arg(*app, char *);
	...
}
```

has been changed to

```
void Str_fmt(int code, va_list_box *box,
	int put(int c, void *cl), void *cl,
	unsigned char flags[], int width, int precision) {
	...
	s = va_arg(box->ap, char *);
	...
}
```

Thanks to [Russ Cox](http://swtch.com/~rsc/) and [Norman Ramsey](http://www.cs.tufts.edu/~nr) for contributing this solution.