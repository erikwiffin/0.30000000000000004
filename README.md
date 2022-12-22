# [0.30000000000000004.com](http://0.30000000000000004.com/)

## Floating Point Math

Your language isn't broken, it's doing floating point math. Computers can only
natively store integers, so they need some way of representing fractional numbers.
This representation has a degree of inaccuracy which is why, more often
than not, `0.1 + 0.2 != 0.3`.

### Why does this happen?

It’s actually rather interesting. When you have a base-10 system (like ours), it can
only express fractions that use a prime factor of the base. The prime factors of
10 are 2 and 5. So 1 / 2, 1 / 4, 1 / 5, 1 / 8, and 1 / 10 can all be expressed cleanly
because the denominators all use prime factors of 10. In contrast, the representations for 1 / 3, 1 / 6, and
1 / 7 all contain repeating digits because their denominators use a prime factor of
3 or 7.

In binary (or base-2), the only prime factor is 2, so you can only express
fractions cleanly which only contain 2 as a prime factor. In binary, 1 / 2, 1 / 4,
1 / 8 would all be expressed cleanly using a finite number of digits, while expressing 1 / 5 or 1 / 10 requires
repeating digits. So 0.1 and 0.2 (1 / 10 and 1 / 5), while cleanly representable in a
base-10 system, contain repeating digits in the base-2 system the computer uses.
When you do math on these numbers with repeating digits, you end up with leftovers which
carry over when you convert the computer's base-2 (binary) number into a more
human-readable base-10 representation.

Below are some examples of sending `.1 + .2` to standard output in a variety of
languages.
