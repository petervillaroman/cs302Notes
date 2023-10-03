# AVL Trees

## Attributes

- Binary Search Tree
- all of its nodes are balanced 

## Balance Factor

- balance factor of a node is the height of the left subtree minus the height of the right subtree

heightLeft - heightRight = balance factor
if balance factor is 0, then the tree is balanced
if balance factor is 1, then the tree is left heavy but **balanced**
if balance factor is -1, then the tree is right heavy but **balanced**

if balance factor is 2, then the tree is left heavy and **unbalanced**
if balance factor is -2, then the tree is right heavy and **unbalanced**

## Rotation

- left rotation
- right rotation

### left rotation

- left rotation is used when the tree is right heavy
- left rotation is used when the tree is right heavy and the right subtree is left heavy
to perform a left rotation on a node, we need to perform a right rotation on the right subtree of the node

```cpp
leftRotation(node* root){
    node* temp = root->right;
    root->right = temp->left;
    temp->left = root;
    return temp;
}
```

### right rotation

- right rotation is used when the tree is left heavy
- right rotation is used when the tree is left heavy and the left subtree is right heavy
to perform a right rotation on a node, we need to perform a left rotation on the left subtree of the node

```cpp

rightRotation(node* root){
    node* temp = root->left;
    root->left = temp->right;
    temp->right = root;
    return temp;
}
```
