The prime factors of 13195 are 5, 7, 13 and 29. What is the largest prime factor of the number?
```r

euler <- function(n) {
  if (n==1) return(NULL)
  if (n==2) return(n)
  l <- 2:n
  i <- 1
  p <- 2
  while (p^2<=n) {
    l <- l[l==p | l%%p!=0]
    i <- i+1 
    p <- l[i]
  }
  return(l)
}

prime.factors <- function (n) {
  factors <- c() 
  primes <- esieve(floor(sqrt(n))) 
  d <- which(n%%primes == 0) 
  if (length(d) == 0) 
    return(n)
  for (q in primes[d]) { 
    while (n%%q == 0) { 
      factors <- c(factors, q)
      n <- n/q } } 
  if (n > 1) factors <- c(factors, n)
  return(factors)
}

print(max(prime.factors(13195)))

```
