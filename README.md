Your language isn't broken, it's doing floating point math.
Computers can only natively store integers, so they need some way of
representing decimal numbers.
This representation comes with some degree of inaccuracy.
That's why, more often than not, .1 + .2 != .3.

http://0.30000000000000004.com/
