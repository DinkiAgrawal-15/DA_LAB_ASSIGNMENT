 The number 512 is interesting because it is equal to the sum of its digits raised to some power: 5 + 1 + 2 = 8, and 83 = 512. Another example of a number with this property is 614656 = 284.
We shall define an to be the nth term of this sequence and insist that a number must contain at least two digits to have a sum.
You are given that a2 = 512 and a10 = 614656.
Find a30.
```r

List<BigInteger> a = new List<BigInteger>();
             
for (int b = 2; b < 400; b++) {
    BigInteger value = b;
    for (int e = 2; e < 50; e++) {
        value *= b;
 
        if (DigitSum(value) == b) {
            a.Add(value);            
        }
        if (a.Count > 50) break;                    
    }
    if (a.Count > 50) break;                    
}
```
