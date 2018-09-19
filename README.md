# LeetCode

## Solutions
Why should we do this again and again?

### Array and Strings

##### A-Marked

- [1. Two Sum](https://leetcode.com/problems/two-sum/description/)
    - 描述：给定一个目标数，返回数组中能使和为目标数的数的索引    
    - 考点：哈希表
    - 思路：遍历数组，目标值与当前索引对应的值求差，并在字典里查找查对应的索引，如果存在则返回，如果不存在，则将当前索引值 - 索引在字典建立映射
- [125. Valid Palindrome](https://leetcode.com/problems/valid-palindrome/)
    - 描述：给定一个字符串，判断该字符串是否是回文，即从前后方向阅读都相同
    - 考点：字符串
    - 思路：通过Python的逆置语法糖逆置，然后字符串匹配
- [8. String to Integer (atoi)](https://leetcode.com/problems/string-to-integer-atoi)
    - 描述：给定一个字符串，将之字符中数字部分转换为整型
    - 考点：字符串
    - 思路：
- [344. Reverse String](https://leetcode.com/problems/reverse-string/description/)
    - 描述：给定一个字符串，将之逆置
    - 考点：字符串
    - 思路：通过Python的逆置语法糖逆置
- [151. Reverse Words in a String](https://leetcode.com/problems/reverse-words-in-a-string/description/)
    - 描述：给定一个字符串，将字符串内的每个字符逆置
    - 考点：
    - 思路：
- [20. Valid Parentheses](https://leetcode.com/problems/valid-parentheses/description/)
    - 描述：括号匹配：{[()]}
    - 考点：栈
    - 思路：遇到左括号入栈，遇到右括号出栈，出栈左括号和右括号如果对不上，则非法，否则合法，最后检查栈是否为空，为空则合法
- [5. Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/description/)
    - 描述：最长回文子串
    - 考点：动态规划
    - 思路：状态转移方程，理清情况，如果左边界等于右边界，则是回文，如果右边界减去左边界等于1，且对应的值相等，则是回文，如果右边界减去左边界大于1，如果对应的值相等，且右边界减去1和左边界加1是回文，则是回文
- [49. Group Anagrams](https://leetcode.com/explore/interview/card/microsoft/30/array-and-strings/200/)
    - 描述：输入一个字符串组成的数组，将字符构成相同的字符串分类后输出
    - 考点：字符串、哈希表
    - 思路：对每个字符串数组排序后建立并维护哈希表
    
- [42. Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/description/)
    - 描述：接雨水，输入为x轴上每一点的墙高度，问能接多少雨水
    - 考点：
    - 思路：一次遍历找到最高墙位置，然后从左和从右向最高墙位置遍历，维护一个临时峰值高度，如果该点的高度小于临时峰值高度，则该点能存的水为临时峰值减去该点高度，否则更新临时峰值为该点高度

### Linked List

##### A-Marked

- [206. Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/description/)
    - 描述：给定一个链表，将之就地逆置
    - 考点：链表
    - 思路：遍历链表，保存当前结点，将当前结点的后继结点更新为前驱结点，然后将前驱结点更新为当前结点
- [141. Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/description/)
    - 描述：给定一个链表，判断该链表是否存在闭环
    - 考点：链表
    - 思路：快慢指针法，快指针初始化为慢指针的后继，然后用慢指针遍历链表，快指针一次更新两次，如果慢指针见底，则无环，如果快慢指针相遇，则闭环
- [2. Add Two Numbers](https://leetcode.com/problems/add-two-numbers/description/)
    - 描述：两链表从头到尾表示数字的低位到高位，将两链表相加
    - 考点：链表
    - 思路：遍历链表相加，注意进位，本次遍历注意结束时不需要创建新节点，再次遍历（如必要），将剩余链表的高位依次添加，注意进位，最后根据进位标志判断是否需要创建新节点
- [445. Add Two Numbers II](https://leetcode.com/problems/add-two-numbers-ii/description/)
    - 描述：两链表从头到位表示数字的高位到地位，不逆序，将链表相加
    - 考点：链表
    - 思路：依次遍历两链表，将链表每个节点的值加和，然后求和重新构造链表
- [21. Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/description/)
    - 描述：将两条已经排序链表合并，已知第一条链表足够长
    - 考点：链表
    - 思路：初始化头结点，定义当前结点为头结点，遍历链表，将第一条与第二条结点中当前较小的结点作为当前节点的后继，然后更新该条当前节点为其后继，最后将多余的结点作为当前节点的后继，然后返回头结点
- [23. Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/description/)
    - 描述：合并K个有序链表
    - 考点：链表
    - 思路：同上
    
### Trees and Graphs

##### A-Marked

- [98. Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/description/)
    - 描述：验证一棵树是否是二叉查找树
    - 考点：二叉查找树的性质（中序遍历有序）
    - 思路：中序遍历，检查中序遍历结果是否有序
- [94. Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/description/)
    - 描述：中序遍历二叉树
    - 考点：二叉树中序遍历，递归，栈
    - 思路：
        - 递归：先递归左孩子，然后添加根节点值，然后递归右孩子
        - 迭代：首先初始化（根节点，未访问）元组并入栈，然后循环，将栈顶出栈，判断节点是否为真，然后判断节点是否已经访问，如果已经访问，则向结果数组添加结果，如果未访问，则依次入栈右、根、左节点，并标记他们的访问情况为否、是、否
- [102. Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/description/)
    - 描述：二叉树层序遍历
    - 考点：二叉树层序遍历
    - 思路：维护一个层节点数组，数组存储当前层所有节点，然后循环（如果层节点数组不为空），遍历层节点所有节点的值，然后将层节点所有非空孩子节点作为新层数组
- [103. Binary Tree Zigzag Level Order Traversal](https://leetcode.com/problems/binary-tree-zigzag-level-order-traversal/description/)
    - 描述：Z字形输出二叉树节点的值
    - 考点：二叉树层序遍历
    - 思路：维护一个层节点数组，数组存储当前层所有节点，然后循环（如果层节点数组不为空），遍历层节点所有节点的值，单次不反转，双次反转，然后将层节点所有非空孩子节点作为新层数组
- [116. Populating Next Right Pointers in Each Node](https://leetcode.com/problems/populating-next-right-pointers-in-each-node/description/)
    - 描述：将一个满二叉树的每一层变成一个链表
    - 考点：二叉树层序遍历
    - 思路：维护一个层节点数组，数组存储当前层所有节点，然后循环（如果层节点数组不为空），遍历层节点所有值，然后串成链表
- [117. Populating Next Right Pointers in Each Node II](https://leetcode.com/problems/populating-next-right-pointers-in-each-node-ii/description/)
    - 描述：将一个二叉树的每一层变成一个链表
    - 考点：二叉树层序遍历
    - 思路：同116思路
- [235. Lowest Common Ancestor of a Binary Search Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/description/)
    - 描述：求二叉查找树两节点的公共祖先
    - 考点：递归
    - 思路：如果根节点的值介于两节点的值间，则返回，否则，如果两节点的值都小于根节点，那么递归本函数，将根节点换为根节点的左孩子，否则右递归
- [236. Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/description/)
    - 描述：求二叉树两节点的公共祖先
    - 考点：二叉树的先根遍历
    - 思路：分别保存先根遍历到两个目标节点的路径，然后依次对比直到不相同
- [105. Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/description/)
    - 描述：已知某二叉树的先根和中根遍历结果，恢复二叉树
    - 考点：递归，二叉树先根和中根遍历的性质
    - 思路：递归，先根遍历结果中，每一个数值都代表一颗子树的根节点，而每一个先根遍历的数值在中根遍历的结果中，其左边所有数值是左子树，右边所有数值是右子树，通过这个性质，用递归求解问题，即如果中根遍历结果不为空，则先根结果出队列，并计算先根结果在中根遍历结果中的索引，以先根结果为根节点，以先根索引为界，递归恢复左右子树

##### B-Marked

- [257. Binary Tree Paths](https://leetcode.com/problems/binary-tree-paths/description/)
    - 描述：给定一颗二叉树，输出根节点到叶子节点的路径，以字符串表示，例如["1->2->5", "1->3"]
    - 考点：递归，二叉树的先根遍历
    - 思路：递归先根遍历二叉树，遇到空节点返回，如果某一节点左右孩子都为空，则序列化一次

### Backtracking

##### A-Marked

- [17. Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/description/)
    - 描述：2-9数字中每个数字对应了电话号码上的几个字母，输入一串2-9的数字，输出数字对应的字母的所有排列组合
    - 考点：回溯、深度优先遍历、递归
    - 思路：注意DFS函数参数设计和递归停止条件，参数应该包含（当前当前索引、数字、当前模式、结果），如果索引等于长度，则应该停止，向结果添加模式，否则，遍历当前数字对应的字母，然后依次DFS，此时索引自增，模式自增当前字母

### Sorting and Searching

##### A-Marked

- [26. Remove Duplicates from Sorted Array](https://leetcode.com/problems/remove-duplicates-from-sorted-array/description/)
    - 描述：就地从排序数组里移除冗余数字
    - 考点：
    - 思路：定义一个"有序尾索引"，该索引永远为有序数组无冗余的"前端"，然后遍历数组，如果数组的"有序尾索引"的值不等于当前值，则有序尾索引自增，然后更新有序尾索引对应的值为当前值，最后返回有序尾索引自增
- [88. Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/description/)
    - 描述：就地合并两个排序后的数组（第一个数组足够长）
    - 考点：分治
    - 思路：从后遍历两个数组，根据当前两索引对应的值的大小，将较大的索引对应的值放进合并索引（m + n - 1)位置中，然后对应索引自减，最后如果第二个数组索引仍然不为，0则继续填充合并索引位置，两索引自减少
- [75. Sort Colors](https://leetcode.com/problems/sort-colors/description/)
    - 描述：三色排序，即0，1，2就地O(n)时间排序，不可用基数排序
    - 考点：双指针
    - 思路：维护三个指针，分别是左，当前，右指针，以当前指针小于等于右指针为条件进入循环，如果当前数字等于2，则将当前数字与右指针交换，然后右指针左移，当前与左指针不动，如果当前数字等于1，左右指针均不动，当前指针自增，如果当前数字等于0，交换当前与左指针的值，然后当前和左指针自增。
- [153. Find Minimum in Rotated Sorted Array](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/description/)
    - 描述：有序数组在某一位被完全反转，例如[0, 1, 2, 3, 4] -> [3, 4, 0, 1, 2]，找出最小元素，无重复元素
    - 考点：二分查找
    - 思路：取左中右索引，如果中值比右值小，则将右索引更新为中索引，如果中值大于右值，则数组在此被反转，将左索引更新为中索引加1
- [154. Find Minimum in Rotated Sorted Array II](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array-ii/description/)
    - 描述：有序数组在某一位被完全反转，例如[0, 2, 2, 3, 4] -> [3, 4, 0, 2, 2]，找出最小元素，可能有重复元素
- [33. Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/description/)
    - 描述：有序数组以某一个元素为枢轴进行旋转，例如[0, 1, 2, 4, 5, 6, 7] -> [4, 5, 6, 7 ,0, 1, 2]，在该数组中寻找一个目标数字，如果存在则返回下标，否则返回-1
    - 考点：二分查找
    - 思路：找到枢轴，然后比较目标数和枢轴的大小，如果目标数大于枢轴，则不存在。如果目标数小于枢轴且大于等于首个元素，则在此区间二分查找，否则在枢轴后至末尾二分查找
- [74. Search a 2D Matrix](https://leetcode.com/problems/search-a-2d-matrix/description/)
    - 描述：在一个二维数组里查找某个目标数，这个二维数组是按下标严格递增的，如存在则返回True，否则返回False
    - 考点：二分查找
    - 思路：按列遍历二维数组的首个元素，找到临界值行，在临界值行的上一行，进行二分查找
- [240. Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/description/)
    - 描述：在一个二维数组里查找某个目标数，这个二维数组是的每一个行是有序的，每一列是有序的，如果存在返回True，否则返回False
    - 考点：二分查找
    - 思路：按列遍历二维数组的首个元素，找到临界值行，遍历0行至临界行进行二分查找

### Dynamic Programming

##### A-Marked

- [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/description/)
    - 描述：输入一个数组代表一个时间段的股票价格，按照时间顺序，找到最佳买入和卖出价格，计算最大收益，如果没有最佳择时，收益为0
    - 考点：
    - 思路：初始化最大收益和最小价格为0，按顺序遍历价格，根据当前价格更新最小价格，根据当前最小价格和当前价格计算收益，根据最大收益和当前收益更新最大收益
- [53. Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
    - 描述：输入一个整型数组，输出最大子串和
    - 考点：动态规划
    - 思路：`dp[index] = max(num, num + dp[index - 1])`其中`dp[index]`为第index个下标的最大子数组和
- [300. Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/description/)
    - 描述：
    - 考点：
    - 思路：

##### B-Marked

- [70. Climbing Stairs](https://leetcode.com/problems/climbing-stairs/description/)
    - 描述：给定一个n层楼梯，n是正数，可以一次上1阶，也可以一次上2阶，输出有多少种上法
    - 考点：动态规划
    - 思路：`dp[i] = dp[i - 1] + dp[i - 2]`