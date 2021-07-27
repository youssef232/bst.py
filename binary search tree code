class BTSNode:
    """A node in the vanilla BST tree."""
    def __init__(self,  parent, k):
        """Creates a node.

               Args:
                   parent: The node's parent.
                   k: key of the node.
               """
        self.parent = parent
        self.key = k
        self.left = None
        self.right = None

    def insert(self, node):
        """Inserts a node into the subtree rooted at this node.

               Args:
                   node: The node to be inserted.
               """
        if node is None:
            return
        if node.key < self.key:
            if self.left is None:
                node.parent = self
                self.left = node
            else:
                self.left.insert(node)
        if node.key > self.key:
            if self.right is None:
                node.parent = self
                self.right = node
            else:
                self.right.insert(node)

    def search(self, k):
        """searches and returns the node with key k from the subtree rooted at this
                node.

                Args:
                    k: The key of the node we want to search for.

                Returns:
                    The node with key k.
                """
        if k == x.key:
            return x
        elif k < self.key:
            if self.left is None:
                return None
            else:
                return self.left.search(k)
        else:
            if self.right is None:
                return None
            else:
                return self.right.search(k)

    def treeMinimum(self):
        """Finds the node with the minimum key in the subtree rooted at this
               node.
                of course, it's by the definition of the BST in the left subtree.
               Returns:
                   The node with the minimum key.
               """
        current = self
        while current.left is not None:
            current = current.left
        return current

    def treeMaximum(self):
        """Finds the node with the maximum key in the subtree rooted at this
                      node.
                       of course, it's by the definition of the BST in the right subtree.
                      Returns:
                          The node with the maximum key.
                      """
        current = self
        while current.right is not None:
            current = current.right
        return current

    def successor(self):
        """Returns the node with the next larger key (the successor) in the BST.
            the smallest key greater than x.key
              """
        if self.right is not None:
            return self.right.treeMinimum()
        current = self
        while current.parent is not None and self == current.parent.right:
            current = current.parent
        return current

    def predecessor(self):
        """Returns the node with the previous smaller key (the predecessor) in the BST.
            the largest key smaller than x.key
              """
        if self.left is not None:
            return self.left.treeMaximum()
        current = self
        while current.parent is not None and self == current.parent.left:
            current = current.parent
        return current

    def delete(self):
        """Deletes and returns this node from the BST."""
        if self.left is None or self.right is None:
            if self is self.parent.left:
                self.parent.left = self.left or self.right
                if self.parent.left is not None:
                    self.parent.left.parent = self.parent
            else:
                self.parent.right = self.left or self.right
                if self.parent.right is not None:
                    self.parent.right.parent = self.parent
            return self
        else:
            s = self.next_larger()
            self.key, s.key = s.key, self.key
            return s.delete()

    def inorderWalk(self):
        """
        prints the keys in the BST inorder(increasing).
        """
        current = self
        if current is not None:
            current.left.inorderWalk()
            print(currnet.key)
            current.right.inorderWalk()


tree = BTSNode(None, 12)
node1 = BTSNode(None, 4)
tree.insert(node1)
node1 = BTSNode(None, 5)
tree.insert(node1)
node1 = BTSNode(None, 2)
tree.insert(node1)
node1 = BTSNode(None, 9)
tree.insert(node1)


