# Asymptotic Complexity

- Running time of an algorithm as a function of input size n **for large n**.
- Expressed using only the **highest-order term** in the expression for the exact running time. 
    - Instead of exact running time, say O(n^2)
- Describes behavior of function in the limit. 
- Written using **Asymptotic Notation**

## Asymptotic Notation

Big O is the most common notation. It is the upper bound of the running time of an algorithm.
Big Theta is the tight bound of the running time of an algorithm.
Big Omega is the lower bound of the running time of an algorithm.

### Big O

- Upper bound of the running time of an algorithm.
- O(n) means that the running time of the algorithm is at most n^2.
- O(n^2) means that the running time of the algorithm is at most n^2.
- O(n^3) means that the running time of the algorithm is at most n^3.
- O(1) means that the running time of the algorithm is constant.

### Big Theta

- Tight bound of the running time of an algorithm.
- Theta(n) means that the running time of the algorithm is at most n^2 and at least n^2.
- Theta(n^2) means that the running time of the algorithm is at most n^2 and at least n^2.
- Theta(n^3) means that the running time of the algorithm is at most n^3 and at least n^3.
- Theta(1) means that the running time of the algorithm is constant.

### Big Omega

- Lower bound of the running time of an algorithm.
- Omega(n) means that the running time of the algorithm is at least n^2.
- Omega(n^2) means that the running time of the algorithm is at least n^2.
- Omega(n^3) means that the running time of the algorithm is at least n^3.
- Omega(1) means that the running time of the algorithm is constant.

Big theta is the intersection of big O and big Omega.


## Proving Asymptotic Complexity

f(n) = 10n^2 - 3n ; g(n) = n^2

prove: f(n) is in big theta of g(n)

For a n0, c1, c2 that exists, c1 * g(n) <= f(n) <= c2 * g(n)

find c1, c2, n0

    f(n) = 10n^2-3n
    c2 = 100; f(n) <= 100g(n)
    c1 = 1; f(n) >= 1g(n)




## Asymptotic Notation in Equations

- Can use aysmptotic notation in equations to replace expressions containing lower-order terms. 

- For example, 

4n^3 + 3n^2 + 2n + 1 = 4n^3 +3n^2 + O(n)

= 4n^3 + O(n^2) = O(n^3)

In equations, O(g(n)) always stand for an **anonymous function** f(n) that is in O(g(n)).
