# Computational Complexity VERY IMPORTANT

```cpp
for (int i =0; i<10; i++){
    cout << i << endl;
}
```

Computational complexity is the # of operations

This means that the complexity of this loop is Big O(n) bc the complexity is linear to the value of n (in this case it's 10)


```cpp
// A nested loop
n = 10; 
m = 7;

for (int i = 0; i < n; i++){
    for (int j = 0; j < m; j++){
        cout << i << " " << j << endl;
    }
}
```

cout is a constant time operation.
this nested loop will do n*m operations.

The big O complexity of this nested loop is O(n*m)

if n > m, then the complexity is O(n^2)

if n < m, then the complexity is O(m^2)

but there is no difference so we just say O(n^2)




It's good to keep in mind that sometimes O(n) can optimize to O(log n)


## constant time operations

- Assigning the value to a variable: x = y
- Mathematical oeprations: x = y + 2 * z
- Comparisons: if (x > max ) max = x
- Accessing a value in an array: x = a[5]

linear: O(n)
Quadratic: O(n^2)
Constant: O(1)


## quadratic operations

```cpp
for(let i=0; I<n; i++){
    for(let j=0; j<m; j++){
        cout << i << " " << j << endl;
    })
}

```

This has a complexity of O(n^2) because 


## O(log n)

2 | 5 | 8 | 12 | 16 | 23 | 38 | 56 | 72 | 91

Given sorted array S, we want to see if value 8 exists in this array. 
If so return the index of value 8 in S. 

### Brute Force method:

t = 8; 

```cpp

for (i = 0; i< s.length; i++){
    if t == S[i] return i;
}

```

Pros: It works for any array

Cons: Not efficient for a sorted array

### Binary Search method:

```cpp
binarySearch(arr, x, low, high)
    if low > high 
        return false
    
    else 
        mid = (low + high ) / 2
            if x == arr(mid)
            return mid
        
        else if x > arr[mid]        # x is on the right side
            return binarySearch(arr, x, mid+1, high)
        
        else                        # x is on the left side
            return binarySearch(arr, x, low, mid-1)
```

Pros: It's efficient for a sorted array

With binary search the process is as follows: 

1. compare the value you're looking for to the middle value of the array
2. if the value you're looking for is greater than the middle value, then you know that the value you're looking for is on the right side of the array
3. if the value you're looking for is less than the middle value, then you know that the value you're looking for is on the left side of the array
4. repeat this process until you find the value you're looking for


if you have an array of 1000 elements, then you can find the value you're looking for in 10 steps.
