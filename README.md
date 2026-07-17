# [0.30000000000000004.com](http://0.30000000000000004.com/)

## Floating Point Math

Your language isn't broken, it's doing floating point math. Computers can only
natively store integers, so they need some way of representing decimal numbers.
This representation has a degree of inaccuracy which is why, more often
than not, `0.1 + 0.2 != 0.3`.

### Why does this happen?

It’s actually rather interesting. When you have a base-10 system (like ours), it can
only express fractions that use a prime factor of the base. The prime factors of
10 are 2 and 5. So 1 / 2, 1 / 4, 1 / 5, 1 / 8, and 1 / 10 can all be expressed cleanly
because the denominators all use prime factors of 10. In contrast, 1 / 3, 1 / 6, and
1 / 7 are all repeating decimals because their denominators use a prime factor of
3 or 7.

In binary (or base-2), the only prime factor is 2, so you can only express
fractions cleanly which only contain 2 as a prime factor. In binary, 1 / 2, 1 / 4,
1 / 8 would all be expressed cleanly as decimals, while 1 / 5 or 1 / 10 would be
repeating decimals. So 0.1 and 0.2 (1 / 10 and 1 / 5), while clean decimals in a
base-10 system, are repeating decimals in the base-2 system the computer uses.
When you do math on these repeating decimals, you end up with leftovers which
carry over when you convert the computer's base-2 (binary) number into a more
human-readable base-10 representation.

Below are some examples of sending `.1 + .2` to standard output in a variety of
languages.

### consider using `%.17g` for `printf` and friends

If your platform supports `printf` and like, it is worth trying `"%.17g"` for output format of floating point numbers.  It does the same as `"%.17f"` when necessary while it keeps the output concise when unnecessary, like `0.5` and `0.9990234375` (`1023/1024`)

### Hexfloat -- How to Exactly Represent Binary Floating Point Numbers

With the introduction of the Hexadecimal Floating-Point Literals (*hexfloat* for short) in [C99] and [C++17], You can now get and/or set the exact values of binary floating point numbers instead of their decimal approximations in platforms that support this feature.

[C99]: https://en.cppreference.com/w/c/language/floating_constant.html
[C++17]: https://en.cppreference.com/w/cpp/language/floating_literal.html

| Decimal | Hexfloat |
|:---------|:----------|
| `0.1` | `0x1.999999999999ap-4`
| `0.2` | `0x1.999999999999ap-3`
| `0.3` | `0x1.3333333333333p-2`
| `0.1+0.2` | `0x1.3333333333334p-2`
| `0.30000000000000004` | `0x1.3333333333334p-2`

To stringify to hexfloat notations, Use `%a` or `%A` in the [printf] format.

[printf]: https://en.cppreference.com/w/c/io/fprintf.html
