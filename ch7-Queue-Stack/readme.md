## 堆栈，队列

在数组中，我们可以通过索引访问随机元素。但是，我们在某些情况下需要限制处理的顺序。接下来介绍两种，`先入后出`和`后入先出`以及两个相对应的线性数据结构，`队列`和`栈`。

那如果想要学习好队列和栈，至少要经历以下几步：
1. 理解`FIFO`和`LIFO`
2. 能够自己实现队列和栈的数据结构
3. 熟悉内置队列和栈结构
4. 使用队列和栈解决常用问题

- [设计循环队列](../Leetcode/622.md)
- [设计循环双端队列](../Leetcode/641.md)
- [有效的括号，栈思想](ch11.py)

### 队列和BFS
`广度优先搜索(BFS)`的一个常见应用是找出从根节点到目标节点的最短路径。

首先将根节点排入队列，然后在每一轮中逐个处理已经在队列中的节点，并将所有邻居添加到队列中。值得注意的是，新添加的节点不会立即遍历，而是在下一轮中处理。

节点的处理顺序与他们添加到队列的顺序是完全相同的，即先进先出。这就是在BFS中使用队列的原因。

- [岛屿的个数](../Leetcode/200.md)
- [打开转盘锁](../Leetcode/752.md)
- [完全平方数](../Leetcode/279.md)

### 栈和DFS
`深度优先搜索(DFS)`也可以用于查找从根节点到目标节点的路径。

首先将根节点push到栈中，然后尝试将第二层第一个节点push到栈中直到最深节点。当回溯时，从栈中弹出最深的节点，这实际是push到栈中的最后一个节点。总的来说，在我们到达一个方向的`最深节点`之后，`回溯`并尝试另一条路径。

节点的处理顺序是完全相反的，就像它们被添加到栈中一样，它们是`后进先出(LIFO)`。这就是DFS中使用栈的原因。

- [岛屿的个数](../Leetcode/200.md)
- [克隆图](../Leetcode/133.md)
- [二叉树的中序遍历](../Leetcode/094.md)
- [目标和](../Leetcode/494.md)

### 栈和队列的互相实现
- [队列实现栈](../Leetcode/225.md)
- [栈实现队列](../Leetcode/232.md)
- [字符串解码](../Leetcode/394.md)