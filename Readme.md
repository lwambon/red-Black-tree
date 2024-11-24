# Red-black tree in Data Structure
The red-Black tree is a binary search tree. The prerequisite of the red-black tree is that we should know about the binary search tree. In a binary search tree, the values of the nodes in the left subtree should be less than the value of the root node, and the values of the nodes in the right subtree should be greater than the value of the root node.

Each node in the Red-black tree contains an extra bit that represents a color to ensure that the tree is balanced during any operations performed on the tree like insertion, deletion, etc. In a binary search tree, the searching, insertion and deletion take O(log2n) time in the average case, O(1) in the best case and O(n) in the worst case.


## Properties of Red-Black tree
Node Colors: Each node is either red or black.  
Root Property: The root is always black.  
Leaf Property: Every leaf (NIL node) is black.  
Red Node Property: If a red node has children, then both children must be black. This prevents two consecutive red nodes along any path.  
Black Height Property: Every path from a node to its descendant NIL nodes must have the same number of black nodes, ensuring balanced paths.  
Balanced Tree: Red-Black Trees are balanced, though not perfectly balanced like AVL trees. The height of the tree is bounded by 2 * log₂(n), ensuring that it remains relatively shallow. 

## Insertion in Red Black tree
### The following are some rules used to create the Red-Black tree:

If the tree is empty, then we create a new node as a root node with the color black.  
If the tree is not empty, then we create a new node as a leaf node with a color red.  
If the parent of a new node is black, then exit.  
If the parent of a new node is Red, then we have to check the color of the parent's sibling of a new node.  
4a. If the color is Black, then we perform rotations and recoloring.  

4b. If the color is Red then we recolor the node. We will also check whether the parents' parent of a new node is the root node or not; if it is not a root node, we will recolor and recheck the node.


## Deletion in Red Back tree
When deleting a node, if the node is black, it may violate the black-height property. The algorithm uses a series of recoloring and rotations to restore the tree's properties
## Rotations
Red-Black Trees use left rotations and right rotations during insertion and deletion to restore balance. These rotations are necessary for maintaining the black height and ensuring that the path from the root to any leaf does not exceed a specific length.
## Advantages:
Efficient Search: Insertion, deletion, and search operations all run in O(log n) time, making it ideal for use in databases and other applications requiring balanced search structures.  
Relatively Simple to Implement: Compared to AVL trees (which require more frequent rotations), red-black trees are easier to implement and maintain, though slightly less strict in balancing.
##  Applications
Database Indexing: Used in many database systems (such as in the B-tree or B+ tree) for efficient searching and sorting.  
Memory Management: Used in garbage collection algorithms (e.g., region-based garbage collection).  
Operating Systems: Red-Black Trees are also used in managing process scheduling or other system-level applications that require fast data retrieval.