---
title: Emacs Lisp
code:
  - (+ .1 .2)
  - (calc-eval ".1 + .2")
  - |-
    (require 'calc-math)
    (math-add (math-read-expr "0.1") (math-read-expr "0.2"))
result:
  - result: 0.30000000000000004
  - '"0.3"'
  - (float 3 -1)
---
