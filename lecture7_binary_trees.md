# Binary Trees yay

## definitions

A tree is an abstract data type
- one entry point, the root
- Each node is either a leaf or an internal node
- An internal node has 1 or more children, nodes that can be reached directly from that internal node. 
- The internal node is said to be the parent of its child nodes


## properties of Trees and Nodes

- siblings: two nodes taht have the same parent
- edge: the link from one node to another
- path length: the number of edges that must be traversed to get form one node to another

## more properties of trees

- depth: the path length from the root of the tree to this node
- height of a node: THe maximum distance (path length) of any leaf from this node

maximum height of a full binary tree with 11 nodes is 5

## binary tree

each node: at most 2 children

## full binary tree

- full binary tree: a binary tree in which every node has either 0 or 2 children.


## complete binary tree

- complete binary tree: a binary tree in which every level, except opossibly the deepest is completely filled. At depth n, the height of the tree, all nodes are as far left as possible. 

leaf node: 0,1,2 children
internal nodes: 2 children

## full complete aka perfect binary tree

- perfect binary tree: a binary tree with all leaf nodes at the same depth. All interal nodes have exactly two children. 

## A binary node class

```cpp

struct node { 
    int data; 
    struct node* left;
    struct node* right;
};

// or 

class Node { 
    public: 
        int data; 
        Node* left;
        Node* right;
};

```


## Binary Tree Traversal

### Preorder traversal ROOT LEFT RIGHT
- Preorder traversal: visit the root node first, then recursively do a preorder traversal of the left subtree, followed by a recursive preorder traversal of the right subtree.

### Inorder traversal LEFT ROOT RIGHT
- Inorder traversal: recursively do an inorder traversal of the left subtree, visit the root node, and finally do a recursive inorder traversal of the right subtree.

### Postorder traversal LEFT RIGHT ROOT
- Postorder traversal: recursively do a postorder traversal of the left subtree and the right subtree followed by a visit to the root node.

## Tree Search: 

### Regular tree 
O(n)

### Sorted tree aka Binary Search Tree 
O(log n)
everything on the left is smaller than the root
everything on the right is larger than the root

each internal node's left child is smaller than the internal node
each internal node's right child is larger than the internal node


## Binary Search Tree

Searching for a value in a binary search tree has a time complexity of O(log n) in the average case and O(n) in the worst case. If it's sorted it's O(log n) in the worst case.

### to find in a BST
```cpp
bool find(binTreeNode *r, int s) { 
    if (r == NULL) return false;
    if (r->data == s) return true;
    if (s < r->data) return find(r->left, s);
    else return find(r->right, s);

}
```

### To find the min and the max

- min: go all the way to the left
- max: go all the way to the right

### inserting in BST

if your value is 18 and the root is 12, you go to the right because 18 is greater than 12.
second root is 15, you go to the right because 18 is greater than 15.

find the location of the leaf node where you can insert the new node.

```cpp
```

### find in BST

## delete in BST 

Harder than other operations because you have to maintain the integrity of the binary search tree's ordering. 

### deleting in the case of a leaf node
```cpp
bool delete(binTreeNode *r, int k) { 
    if(root == null ) return true;
    if (root->left == null && root->right = null) {
        free(root);
        return true;
    }
    else{
        delete(r->left);
        delete(r->right);
    }
}
```

### deleting in the case of a node with two children


2 approaches:

1. Left subtree: find maximum node 
2. Right subtree: find minimum 

```cpp

```
