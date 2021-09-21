# AVLTREE
Self Balancing Binary Search Tree HLS Implementation

:star: Star me on GitHub — it motivates me a lot!

## Overview
ADTs (Abstract Data Type) are commonly used in software to abstract out the implementation details. These ADTs can be used in HLS for hardware design, as offset based structures allow heterogenity. (Offset – is a way of identifying a location given a starting point.)
Here we can see an implementation of the AVL Tree (Self Balancing Binary Search Tree) by using the abstract data type- ADT.

## [AVL Trees](https://en.wikipedia.org/wiki/AVL_tree) 
- It is a Binary Search Tree (BST)
- With additional balance property
- Height of the left sub-tree and height of the right sub-tree differ by at most 1.

## Balance Condition
- For a tree to be balanced, the value has to only be -1, 0, 1. <br />
- Balance(tree) = height of (Tree. Left) – height of (Tree. Right) <br />
         `[bf = hl – hr = {-1,0,1} ; |bf| = |hl-hr| =< 1]`
         
![AVL Tree with balance factors (green)](https://en.wikipedia.org/wiki/AVL_tree#/media/File:AVL-tree-wBalance_K.svg)

## Determining which rotation to use
- If the unbalance node’s height is:<br />
  - Positive: Left Side (Example: Height = 2)<br />
 	  - If the left node’s height is:<br />
	       - Positive: LL Rotation (Example: Height = 1)<br />
	       - Negative: LR Rotation (Example: Height = -1)<br />
  - Negative: Right Side (Example: Height = -2)<br />
 	  - If the right node’s height is:<br />
	       - Positive: RL Rotation (Example: Height = 1)<br />
	       - Negative: RR Rotation (Example: Height = -1)<br />

Note:
-	Always place the child to the correct parent after each rotation!<br />
-	RR Rotation and LL rotation are considered to be a single rotation<br />
  - It is dealing with the outside insertions.<br />

-	RL rotation and LR rotation are consider to be a double rotation<br />
  - It is dealing with the inside insertions.
