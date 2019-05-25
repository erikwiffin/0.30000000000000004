---
layout: post
title: "Common Lisp"
code:
  - '(+ .1 .2)'
  - '(+ 1/10 2/10)'
  - '(+ 0.1d0 0.2d0)'
  - '(- 1.2 1.0)'
result:
  - 0.3
  - 3/10
  - 0.30000000000000004d0
  - 0.20000005
---
CL’s spec doesn’t actually even require radix 2 floats (let alone specifically 32-bit singles and 64-bit doubles), but the high-performance implementations all seem to use IEEE floats with the usual sizes. This was tested on SBCL and ECL in particular.
