# pointer for any variable 

int num;
int *p;

p = & num;

num = 20 ---> *p = 20


# pointer & class 

``` cpp

class A {
public: 
    int n;
    char c;
    string s;
    int r[10];
}
```

class A is a user defined **type**. 

q -> n  = 5   ===   (*q)n = 5

**arrow is preferred** 

q->n = 5
q->c = 'l'
q->s = 'hello'
q->r[0] = 42,
q->r[9] = 10;

# pointer & Array class

A b[10];

an array of class A. so every index of the array is its own class 

int n; char c; etc...



```cpp

A b[10];

A *ptr;

ptr = b;
ptr[0]->n = 10;
ptr[9]->s = "wed",
```

