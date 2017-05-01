---
layout: post
title: "Mathematica"
code: 0.1 + 0.2
result: 0.3
---
Mathematica has a fairly thorough internal mechanism for dealing with
[numerical precision](https://reference.wolfram.com/language/tutorial/NumericalPrecision.html) and supports arbitrary precision.

[By default](https://reference.wolfram.com/language/tutorial/MachinePrecisionNumbers.html), the inputs <code>0.1</code> and <code>0.2</code> in the example are taken to have [MachinePrecision](https://reference.wolfram.com/language/ref/MachinePrecision.html).
At a common <code>MachinePrecision</code> of <code>15.9546</code> digits, <code>0.1 + 0.2</code> actually has a [FullForm](https://reference.wolfram.com/language/ref/FullForm.html) of <code>0.30000000000000004`</code>, but is printed as <code>0.3</code>.

Mathematica supports rational numbers: <code>1/10 + 2/10</code> is <code>3/10</code> (which has a <code>FullForm</code> of <code>Rational[3, 10]</code>).
