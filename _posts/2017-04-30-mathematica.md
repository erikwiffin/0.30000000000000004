---
title: Mathematica
code: 0.1 + 0.2
result: 0.3
---

Mathematica has a fairly thorough internal mechanism for dealing with [numerical
precision][1] and supports arbitrary precision.

[By default][2], the inputs `0.1` and `0.2` in the example are taken to have
[MachinePrecision][3]. At a common `MachinePrecision` of `15.9546` digits,
`0.1 + 0.2` actually has a [FullForm][4] of `0.30000000000000004`, but is
printed as `0.3`.

Mathematica supports rational numbers: `1/10 + 2/10` is `3/10` (which has a
`FullForm` of `Rational[3, 10]`).

[1]: https://reference.wolfram.com/language/tutorial/Numbers.html#21155
[2]: https://reference.wolfram.com/language/tutorial/MachinePrecisionNumbers.html
[3]: https://reference.wolfram.com/language/ref/MachinePrecision.html
[3]: https://reference.wolfram.com/language/ref/FullForm.html
