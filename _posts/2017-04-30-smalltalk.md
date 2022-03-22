---
title: Smalltalk
code:
  - (1/10) + (2/10).
  - '0.1 + 0.2.'
  - 0.1s17 + 0.2s17.
result: 
  - (3/10)
  - '0.30000000000000004'
  - 0.30000000000000000s17
---

Smalltalk uses fractions by default in most operations; in
fact, standard devision results in fractions, not floating
point numbers. Squeak and similar Smalltalks provide "scaled
decimals" that allow fixed-point real numbers (`s`-suffix
indicating precision places).
