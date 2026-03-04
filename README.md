# Tree-DS
Practice program
class Node:
    def __init__(self, data):
        self.data = data
        self.left = None
        self.right = None

# Preorder function
def preorder(root):
    if root is None:
        return
    print(root.data, end=" ")   # Print root
    preorder(root.left)         # Visit left subtree
    preorder(root.right)        # Visit right subtree

# Example usage
root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.left.right = Node(5)

preorder(root)
Output:
1 2 4 5 3
