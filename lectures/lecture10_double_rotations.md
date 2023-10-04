# double rotations for AVL trees

## This is a left heavy tree
 

### 50 25 75 50 80 20 30 10 15

this requires a double rotation. 

first, we need to perform a left rotation on the right subtree of the root node. 

then, we need to perform a right rotation on the root node.



## This is a right heavy tree 

### 50 , 25, 75, 20, 90 , 70, 100, 95

this requires a double rotation 
first, we need to perform a right rotation on the left subtree of the root node. 
then, we need to perform a left rotation on the root node.


this is right heavy => right rotation THEN left rotation



## This is a left heavy tree

## 50, 25, 75, 80, 30, 20, 22, 10, 24

this requires a double rotation
first, we need to perform a left rotation on the right subtree of the root node.
then, we need to perform a right rotation on the root node.

## SUMMARY 

Single rotation for a left heavy tree: is a right rotation.

Single rotation for a right heavy tree: is a left rotation.

Double rotation for a left heavy tree: is a left rotation on the **right subtree of the root cause node**, then a right rotation on the **root cause node**

Double rotation for a right heavy tree: is a right rotation on the left subtree of the root node, then a left rotation on the root node

