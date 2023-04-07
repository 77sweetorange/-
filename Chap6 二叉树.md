# Day 14

## 二叉树理论基础

种类：满二叉树；完全二叉树；二叉搜索树；平衡二叉搜索树

存储方式：链式存储（使用指针）；顺序存储（使用数组）

遍历方式1：深度优先遍历（前序、中序、后序 —— 中间节点的顺序位置差异） 

遍历方式2：广度优先遍历（层次遍历）

```
# Definition for a binary tree node.
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```

## 144 94 145 递归遍历

debug: res为全局变量，放置在子函数外，否则会循环res = [] 

递归写法三要素：

Step1 确定递归函数的参数和返回值

Step2 确定终止条件 如果当前遍历的节点为空，则return

Step3 确定单层递归的逻辑（中左右、左中右、左右中）

## 144 94 145 迭代遍历

[TreeNode] 表示由多个TreeNode的节点组成的列表

加入列表的是数值node.val而不是节点node

# Day 15

## 102 层序遍历

经典模版！！！

## 226 翻转二叉树

指针交换而非数值交换

单层递归的逻辑：前序遍历 —— 先交换左右孩子节点，然后反转左子树，反转右子树

## 101 对称二叉树

一个树的遍历顺序是左右中，一个树的遍历顺序是右左中

镜像 比较二叉树的外侧是否对称（left.left = right.right） 以及 内侧是否对称（left.right = right.left）
