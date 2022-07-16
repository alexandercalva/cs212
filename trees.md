### Introduction

Trees are the most used data structure in programming and at the same time the most complex to understand. Trees are characterized by storing their nodes in a hierarchical way and not in a linear way as do lists, stacks, queues, etc.
#### Binary Trees
A binary tree is a tree that has no more than two nodes below its root. After these two nodes subtrees can be created. The nodes that reach the end of the level of the entire tree are known as leaf nodes. Nodes that contain two nodes below their level are known as parent nodes and those below them are called child nodes. Every binary tree has a single root node.

![image](https://user-images.githubusercontent.com/38995873/179334715-3c30db01-1422-46fa-95c4-958abf55a987.png)

#### Binary search Trees
This type of binary tree maintains some interesting rules to order the value of the nodes entered into it. In other words, nodes with a value less than the last added node are placed to the left of it. If, on the other hand, the value of the entered node is greater, it is located to the right of it. This goes in sequence through the levels constituted in the tree. This allows to obtain an ordered binary tree.

#### Balanced binary Trees
This type of binary tree maintains some interesting rules to order the value of the nodes entered into it. In other words, nodes with a value less than the last added node are placed to the left of it. If, on the other hand, the value of the entered node is greater, it is located to the right of it. This goes in sequence through the levels constituted in the tree. This allows to obtain an ordered binary tree.

![image](https://user-images.githubusercontent.com/38995873/179334901-4345c232-2736-4d6c-b1ca-7efadda92776.png)


#### Balanced binary Trees
A balanced binary search tree is represented by the height that exists between any two subtrees. Entering new nodes can cause an imbalance in a binary tree. To correct this problem, some algorithms have been created, such as the red black trees and AVL (Adelson-Velskii and Landis) trees. The following figure shows an AVL tree.

![image](https://user-images.githubusercontent.com/38995873/179335628-4de57a34-7b84-462c-80d8-a48674d18da4.png)

If we add a node with the value 13 we see how the tree is unbalanced.

![image](https://user-images.githubusercontent.com/38995873/179335665-86542c1b-9ad3-4712-97db-284f3390fb37.png)

Now using the AVL algorithm this problem is going to be corrected as seen in the following image.

![image](https://user-images.githubusercontent.com/38995873/179335695-c09add0b-7f78-46a1-a371-d2c353c5e1f1.png)

#### Example

def insert(self, data):

	"""
	Insert 'data' into the BST.  If the BST
	is empty, then set the root equal to the new 
	node.  Otherwise, use _insert to recursively
	find the location to insert.
	"""
  
	if self.root is None:
		self.root = BST.Node(data)
	else:
		self._insert(data, self.root)  # Start at the root


def _insert(self, data, node):

	"""
	This function will look for a place to insert a node
	with 'data' inside of it.  The current subtree is
	represented by 'node'.  This function is intended to be
	called the first time by the insert function.
	"""
  
	if data < node.data:
		# The data belongs on the left side.
		if node.left is None:
			# We found an empty spot
			node.left = BST.Node(data)
		else:
			# Need to keep looking.  Call _insert
			# recursively on the left subtree.
			self._insert(data, node.left)
	elif data >= node.data:
		# The data belongs on the right side.
		if node.right is None:
			# We found an empty spot
			node.right = BST.Node(data)
		else:
			# Need to keep looking.  Call _insert
			# recursively on the right subtree.
			self._insert(data, node.right)
      
 #### Problem to Solve
INSERT UNIQUE VALUES ONLY
Update the _insert function of the BST class to only allow unique values to be added to the tree (thus creating a sorted set). The _insert function is already written to correctly insert values into the BST. However, the current implementation will cause duplicate values to be added to the tree.

def _insert(self, data, node):

        """
        This function will look for a place to insert a node
        with 'data' inside of it.  The current sub-tree is
        represented by 'node'.  This function is intended to be
        called the first time by the insert function.
        """
        
        if data < node.data:
            # The data belongs on the left side.
            if node.left is None:
                # We found an empty spot
                node.left = BST.Node(data)
            else:
                # Need to keep looking.  Call _insert
                # recursively on the left sub-tree.
                self._insert(data, node.left)
        else:
            # The data belongs on the right side.
            if node.right is None:
                # We found an empty spot
                node.right = BST.Node(data)
            else:
                # Need to keep looking.  Call _insert
                # recursively on the right sub-tree.
                self._insert(data, node.right)
                
                
