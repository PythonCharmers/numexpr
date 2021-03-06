==========================
 Announcing Numexpr 2.3
==========================

Numexpr is a fast numerical expression evaluator for NumPy.  With it,
expressions that operate on arrays (like "3*a+4*b") are accelerated
and use less memory than doing the same calculation in Python.

It wears multi-threaded capabilities, as well as support for Intel's
MKL (Math Kernel Library), which allows an extremely fast evaluation
of transcendental functions (sin, cos, tan, exp, log...)  while
squeezing the last drop of performance out of your multi-core
processors.  Look here for a some benchmarks of numexpr using MKL:

https://github.com/pydata/numexpr/wiki/NumexprMKL

Its only dependency is NumPy (MKL is optional), so it works well as an
easy-to-deploy, easy-to-use, computational engine for projects that
don't want to adopt other solutions requiring more heavy dependencies.

What's new
==========

The repository has been migrated to https://github.com/pydata/numexpr.
All new tickets and PR should be directed there.  Also, a `conj()`
function for computing the conjugate of complex arrays has been added.
Thanks to David Menéndez.  See PR #125.

Finallly, we fixed a DeprecationWarning derived of using ``oa_ndim ==
0`` and ``op_axes == NULL`` when using `NpyIter_AdvancedNew()` and
NumPy 1.8.  Thanks to Mark Wiebe for advise on how to fix this
properly.

Many thanks to Christoph Gohlke and Ilan Schnell for his help during
the testing of this release in all kinds of possible combinations of
platforms and MKL.

In case you want to know more in detail what has changed in this
version, see:

https://github.com/pydata/numexpr/wiki/Release-Notes

or have a look at RELEASE_NOTES.txt in the tarball.

Where I can find Numexpr?
=========================

The project is hosted at GitHub in:

https://github.com/pydata/numexpr

You can get the packages from PyPI as well (but not for RC releases):

http://pypi.python.org/pypi/numexpr

Share your experience
=====================

Let us know of any bugs, suggestions, gripes, kudos, etc. you may
have.


Enjoy data!


.. Local Variables:
.. mode: rst
.. coding: utf-8
.. fill-column: 70
.. End:
