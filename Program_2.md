Q2. The sum of the squares of the first ten natural numbers is, 12+22+...+102=385 The square of the sum of the first ten natural numbers is, (1+2+...+10)2=552=3025 Hence the difference between the sum of the squares of the first ten natural numbers and the square of the sum is 3025−385=2640 .Find the difference between the sum of the squares of the first one hundred natural numbers and the square of the sum.
```r

sum=0;
sq=0;
res = 0;
n = 10;

sum = n*(n+1)/2;
sq=(n*(n+1)*(2*n+1))/6;
res=sum*sum-sq;
print(res)
```
