### Binary Tree

#### Binary search Trees（BTS）sort

```
for i <- 1 to n
	do tree - Insert(T,A[i])
inorder Traversal (In order Tree Walk)
1.recursively walk the left subtree
2.print out root
3.recursively walk the right subtree
```

Example: A=3,1,8,2,6,7,5

Binary Search Tree

![image-20211005221332059](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20211005221332059.png)

In order traversal: 1,2,3,5,6,7,8

```python
#Binary Tree Inorder Traversal
#Input: root = [1,null,2,3]
#Output: [1,3,2]
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
#Inorder Traversal
class Solution:
    def inorderTraversal(self, root: TreeNode) -> List[int]:
        result = []
        def traversal(root: TreeNode):
            if root == None:
                return
            traversal(root.left)#left
            result.append(root.val)#root
            traversal(root.right)#right
        traversal(root)
        return result
#Preorder Traversal
Class Solution:
	def preorderTraversal(self, root: TreeNote) -> List[int]:
		result = []
		if root == None:
			return
		result.append(root.val)#root
		traversal(root.left)#left
		traversal(root.right)#right
	traversal(root)
	return result
#postorder Traversal
Class Solution:
	def preorderTraversal(self, root: TreeNote) -> List[int]:
		result = []
		if root == None:
			return
		traversal(root.left)#left
		traversal(root.right)#right
		result.append(root.val)#root
	traversal(root)
	return result
```

> Time: O(n) for walk
>
> n Tree-inserts	(Ω(nlgn))
>
> Worse Case: already sorted Time = ∑ depth(x) θ(n²)
>
> Lucky Case: balanced O(lgn) height =>O(nlgn) time

#### Relation to QuickSort

BST & QuickSort(stable)

make the same comparisons but in a different order



