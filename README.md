# QuickDivision

  a / b
= (1 / b) * a
= (2^e / b) * a / 2^e

  INT(a / b)
= INT((2^e / b) * a / 2^e)
= INT(((2^e + c) / b) * a / 2^e)
= INT(a / b + c * a / (b * 2^e))

=> c * a / (b * 2^e) < 1 / b
=> c * a < 2^e
