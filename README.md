Download Link: https://assignmentchef.com/product/solved-cs1332-homework-4-binary-search-trees
<br>
You are to code a binary search tree. A binary tree is a collection of nodes, each having a data item and a reference pointing to the left and right child nodes. What makes a binary tree a binary search tree is that it must follow the order property: for any given node, its left child and all of its children must be less than the current node while its right child and all of its children must be greater than the current node. In order to compare the data, all elements added to the tree must implement Java’s generic Comparable interface.

It will have two constructors: the no-argument constructor (which should initialize an empty tree), and a constructor that takes in data to be added to the tree, and initializes the tree with this data. Any attempts to add data that is already in the tree should be ignored (the tree shouldn’t be changed, and the duplicate item shouldn’t get added).

You may import Java’s LinkedList/ArrayList classes for the 4 traversal methods, but only for these methods.

Recursion

Since trees are naturally recursive structures, all methods that are not <em>O</em>(1) <strong>must be implemented recursively</strong>, except for level order traversal. You’ll also notice that a lot of the public method stubs we’ve provided do not contain the parameters necessary for recursion to work, so these public methods act as “wrapper methods” for the user to use. These wrapper methods will just call another private helper method that is recursive. To reiterate, <strong>do not change the method headers for the provided methods.</strong>

For methods that change the structure of the tree in some way, we highly recommend you use a technique taught in class called pointer reinforcement. It’s not required, but it will make the homework cleaner, and it’ll also help greatly when we get to a later homework.

<strong>Nodes</strong>

The binary search tree consists of nodes. The BSTNode class will be given to you; do not modify it.

Methods

You will implement all standard methods for a Java data structure (add, remove, etc.) in addition to a few other methods. Some of these methods are functions that you’d expect from a BST (such as the traversals) while some of the other ones serve more as practice BST recursion problems for you.

Traversals

You will implement 4 different ways of traversing a tree: pre-order traversal, in-order traversal, postorder traversal, and level-order traversal. The first 3 MUST be implemented recursively; level-order is best implemented iteratively. For a level-order traversal, you may use Java’s Queue interface (and an implementing class for it such as LinkedList).

Height

You will implement a method to calculate the height of the tree. The height of any given node is max(left node’s height, right node’s height) + 1. A leaf node has a height of 0. Based on this recursive definition, this means that null nodes would have a height of -1.

Comparable

As stated, the data in the BST must implement the Comparable interface. As you’ll see in the java files, the generic typing has been specified to require that it implements the Comparable interface. You use the interface by making a method call like data1.compareTo(data2). This will return an int, and the value tells you how data1 and data2 are in relation to each other.

<ul>

 <li>If positive, then data1 &gt; data2.</li>

 <li>If negative, then data1 &lt; data2.</li>

 <li>If zero, then data1 equals data2.</li>

</ul>

Do note that the returned value can be any integer in Java’s int range, not just -1, 0, 1 as you may have seen in some examples.