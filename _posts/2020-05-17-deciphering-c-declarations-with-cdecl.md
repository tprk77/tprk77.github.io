---
title: Deciphering C Declarations with 'cdecl'
---

Sometimes C declarations can be a little tricky to pull apart.
Especially when it comes to pointers to functions, arrays, and
pointers to functions returning arrays of pointers to functions. Throw
in some `const` and you might really need some help. Thankfully,
there's a utility for that.

If you've read Kernighan and Ritchie's [*The C Programming
Language*][knrc], you might remember `cdecl`. There's an incomplete
version of it in the "Complicated Declarations" section of the book.
`cdecl` is a handy utility that explains C declarations:

```
cdecl> explain const char * const * const argv
declare argv as const pointer to const pointer to const char

cdecl> explain void (*(*foo)(void)[3])(void)
declare foo as pointer to function (void) returning array 3 of pointer
to function (void) returning void
```

If you're on Ubuntu, there's a package you can install:

```
$ sudo apt-get install cdecl
```

If you're on the go, there's also a handy web version:

* [**https://cdecl.org**][cdeclweb]

Happy C programming!


{% comment %} References {% endcomment %}

[knrc]: https://www.amazon.com/C-Programming-Language-2nd-Edition/dp/0131103628
[cdeclweb]: https://cdecl.org
