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

Big-Oh notation: O(g(n)) denotes the set of functions that grow no faster than g, 

Big-Omega notation: Ω(g(n)) denotes the set of functions that grow no slower than g, so Ω is for lower bounds

Big-Theta notation
