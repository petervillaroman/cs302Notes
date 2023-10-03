# linked list

## defining a linked list

```cpp
Struct Node { 
    typedef double Item;
    Item data;
    Node *link;
};

Node *head_ptr;
Node *tail_ptr;

```

### Steps:

1. define a node 

```cpp
Struct Node{
    
    int value; // (-> typedef int Item; --> Item value;) 
    node *ptr;
}
```

## doubly linked list

```cpp

struct Dnode { 
    string name; // (-> typedef strng Item --> Item name)
    Dnode *prev, *next;
};

Node* NodePtr;

```

### doubly linked list operations

- insertNode(NodePtr Head, int item)
- deleteNode(NodePtr Head, int item)
- searchNode(NodePtr Head, int item)
- print 

### Doubly Linked Lists w/ Dummy Head Node

easier to deal with doubly linked lists if you use a dummy node which's prev links to the last node and which's next links to the first node. 

prev->lastNode| head |next->firstNode (hopefully this makes sense)

- deleting a node with doubly linked list: 

 ```cpp
    (Cur->prev)->next = Cur->next; 
    (Cur->next)->prev = Cur->prev;
    delete Cur;
```

Creating a head function makes it so that deletes, in any part of the linked list, only requires one delete function. 

## delete node function
```cpp
void deleteNode(NodePtr Head, int item) { 
    NodePtr Cur;
    Cur = searchNode(Head,item);
    if(Cur !=Null) { 
        Cur->prev->next = Cur->next;
        Cur->next->prev = Cur->prev;
        delete Cur;
    }
}
```

## inserting a node

insert a node New after dummy node and before Cur

```cpp
    New->next = Cur; // new node's next points to current
    New->prev = Cur->prev; // new node's prev points to current's preview
    Cur->prev = New; // current' prev points to New node
    (New->prev)->next = New; // New node's previous's next is New 

```


## inserting a node New to empty list (with Cur pointing to dummy head node)

```cpp
    New->next = Cur;
    New->prev = Cur->prev;
    Cur->prev = New;
    (New->prev)->next = New;

```







