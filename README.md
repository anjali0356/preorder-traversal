# preorder-traversaldef preorderTraversal(self, root: Optional[TreeNode]) -> List[int]:
	self.ans = [] # answer

	def dfs(node): # depth-first-search helper method
		if node: # we only care about nodes that exist
			self.ans.append(node.val) # add this node to the traversal
			dfs(node.left) # add the preorder traversal of the left node
			dfs(node.right) # add the preorder traversal of the right node

	dfs(root) # start at the top
	return self.ans
