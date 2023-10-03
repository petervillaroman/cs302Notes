# monotonicity


- f(n) is 
    - monotonically increasing if m <= n -> f(m) <= f(n)
    - monotonically decreasing if m <= n -> f(m) >= f(n)
    - strictly increasing if m < n -> f(m) < f(n)
    - strictly decreasing if m < n -> f(m) > f(n)

[Link to chat gpt summary](https://chat.openai.com/c/fa71f929-c940-448a-9c22-dbd6546f8011)


## Polylogarithms

-lg(n!) = O(n lg n)
    - proven using Stirling's approximation (in the text) for lg(n!).

# Exercise

for (int i = 0; i < n; i++) {
    for (int j = 0; j < i; j++) {
        cout << "hello"; 
    }
}

O(n^2)

if n = 5

when i = 0 -> j = nothing
when i = 1 -> j = 0
when i = 2 -> j = 0, 1
when i = 3 -> j = 0, 1, 2
when i = 4 -> j = 0, 1, 2, 3

so the number of times the inner loop runs is 1 + 2 + 3 + 4 = 10

upper bound is n(n-1)/2 = O(n^2)



for (int i = 0 ; i< n; i = i*2) { 
    cout << "hello";
}

o(log n)

N = 10 

i = 1 = 2^0
i = 2 = 2^1
i =4 = 2^2
i = 8 = 2^3




```cpp
for (int i = n; i > 0; i = i/2){
    for (int j = 0; j <1; j++){
        cout << "hello";
    }
}
```
O(n)

```cpp
for (int i = N; i > 0; i = i/3){
    for (int j = 0; j < i; j++){
        cout << "hello";
    }
}
```

N = 27

i = 27; j=0...26; = 3^3
i = 9; j=0...8 = 3^2
i = 3; j=0...2 = 3^1
i = 1; j=0 = 3^0

Computational complexity = # of operations
the total number of times the inner loop runs is 27 + 9 + 3 + 1 = 40

total # of operations is the summation of i = 0 to 3 of 3^i = 40

Av1(1-q^n) / 1-q = 1(1-3^4) / 1-3 = 40

number of operations is 1/2(3^n-1)

3^2n < N
n < log3(N)



O(n)