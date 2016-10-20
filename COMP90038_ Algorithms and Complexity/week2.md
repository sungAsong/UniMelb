## Growth Rate & Algorithm Efficiency

Resouces
 - time
 - space

Running time depends on:
 - The complexity of the algorithm used (function of n)
 - Input to the program (assume input size is n)
 - Underlying machine, incluede memory architecture (ignore)
 - Language/compiler/operating system (ignore)


c is the cost of basic operation

g(n) is the times of operation with input size n

the runnging time t(n) ≈ c·g(n)

Problem v.s. size measurement v.s. basic operation

| Problem | size measurement | basic operation |
| :------:| :------: | :------: |
| search in list of n items | n | key comparison |
| multiply two matrics of floats | rows times coloumns | float multiplication |
| compute a<sup>n</sup> | logn | float multiplication |
| graph problem | number of nodes and edges | visiting a node |


Worst-case: analysis makes the most adverse assumptions about input.

Best-case: analysis makes optimistic assumptions.

Average-case: analysis aims to find the expected running time across all possible input of size n. (Note: This is not an average of the worst and best cases.)

*Amortised* analysis takes the context of running an algorithm into account and calculates cost *spread over many runs*.


Asymptotic Analysis: Growth Rate
 - ignore constant factors
 - ignore small input size


1 < logn < n<sup>ε</sup> < n<sup>c</sup> < n<sup>logn</sup> < n<sup>n</sup>  

(where 0 < ε < 1 < c)


Big-Oh notation: O(g(n)) denotes the set of functions that grow no faster than g, so O is for upper bounds

Big-Omega notation: Ω(g(n)) denotes the set of functions that grow no slower than g, so Ω is for lower bounds

Big-Theta notation: Θ(g(n)) denotes the exact order of growth


limit(n->∞) t(n)/g(n)

often use L’Hˆopital’s rule to compare two growth rate.
 - 0 implies t grows asymptotically slower than g
 - c implies t and g have same order of growth
 - ∞ implies t grows asymptotically faster than g


Analysis general functions: leave out


Analysis recursive functions:

for example:

```
function F(n)
    if n=0 then
        return1 
    else 
        return F(n − 1) · n
```

**recursion form**:

M(0) = 0

M(n) = M(n−1)+1 for n > 0

**closed form**, that is, one without recursion

M(n) = [M(n − 2) + 1] + 1 = M(n − 2) + 2

... = [M(n − 3) + 1] + 2 = M(n − 3) + 3 = . . . = M(n − n) + n = n

so closed form is M(n) = n



some formula:

due to 

log<sub>a</sub> x = (log<sub>a</sub> b)(log<sub>b</sub> x)

log<sub>2</sub> n = O(ln n)

ln n = O(log<sub>2</sub> n)

so that

log n<sup>c</sup> = O(log n)



O(f(n)) + O(g(n)) = O(max{f(n), g(n)})

c · O(f(n)) = O(f(n))

O(f(n)) · O(g(n)) = O(f(n) · g(n))


n! = O(n<sup>n+(1/2)</sup>)


sum(n): i<sup>2</sup> = n/3(n+1/2)(n+1)


sum(n): 2i + 1 = (n+1)<sup>2</sup>


sum(n): 1/i = O(log n)
