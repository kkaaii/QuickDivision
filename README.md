# QuickDivision

  a / b
= (1 / b) * a
= (2^e / b) * a / 2^e

  INT(a / b)
= INT((2^e / b) * a / 2^e)
= INT(((2^e + c) / b) * a / 2^e)  [c = 0, or c = b - mod(2^e, b)]
= INT(a / b + c * a / (b * 2^e))

=> c * a / (b * 2^e) < 1 / b
=> c * a < 2^e

## Samples 
 b  |  e  |  c  | ok?
--- | --- | --- | ---
 3  |  32 |  2  | no (when a = 2^32 - 1)
 3  |  33 |  1  | yes

## Algorithm
e = INT(log2(b)) + 33
