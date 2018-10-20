
## Dynamic Programming
### Concepts
* Definition: Simplifying a complicated problem by breaking it down into simpler sub-problems in a recursive manner
* Key point is that it **reuses** the results from othre sub-problems

### Fibonacci Sequence is one of best example of dynamic programming
* An example of recursive function is below
* Computational cost is very expensive : O(2^n)
```
def naive_fibo(n):
    if n==1 or n==2: return(n)
    return naive_fibo(n-1)+naive_fibo(n-2)
```
* The solution with DP is following
* Computational cost is much chipper: O(n)
```
def dynamic_fibo(n):
    fibo_seq = [1,1]
    for i in range(2, n):
        fibo_seq.append(sum(fibo_seq[i-2:i]))
    #print(fibo_seq)
    return fibo_seq[-1]
```
* While engineering features, dynamic programming may be useful. 

### Another example
* Q. Let $$ f(n) = \sum_{i=1}^{n} \frac{1}{\sum_{j=1}^{i}
