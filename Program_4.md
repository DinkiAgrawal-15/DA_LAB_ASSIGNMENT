 The following iterative sequence is defined for the set of positive integers:
n → n/2 (n is even)
n → 3n + 1 (n is odd)
Using the rule above and starting with 13, we generate the following sequence:
13 → 40 → 20 → 10 → 5 → 16 → 8 → 4 → 2 → 1
It can be seen that this sequence (starting at 13 and finishing at 1) contains 10 terms. Although it has not been proved yet (Collatz Problem), it is thought that all starting numbers finish at 1.
Which starting number, under one thousand, produces the longest chain?
```r
collatz.chain <- function(n) {
    chain <- vector()
    i <- 1
    while (n != 1) {
        if (n%%2 == 0)
            n <- n / 2
        else
        n <- 3 * n + 1
        chain[i] <- n
        i <- i + 1
    }
    return(chain)
}
answer <- 0
collatz.max <- 0
for (n in 1:1E6) {
    collatz.length <- length(collatz.chain(n))
    if (collatz.length > collatz.max) {
        answer <- n
        collatz.max <- collatz.length
    }
}
print(answer)
```
