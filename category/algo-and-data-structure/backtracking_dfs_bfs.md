# 1. knowledge
## 1.1 Difference between backtracking and dfs
>backtracking handles an implicit tree and DFS deals with an explicit one. 
backtracking is DFS for implicit tree, while DFS is backtracking without pruning
-- https://stackoverflow.com/questions/1294720/whats-the-difference-between-backtracking-and-depth-first-search

## 1.2 BFS
如何初始化bfs的queue？超级源点、排序等
如何不走重复的点？set记录走过的点的坐标
如何从当前点到adjacent点？queue、set都记录坐标

# 2. Category
![](/lc/images/backtrack-search.png)

## 2.1 Backtracking
最简单的限定组合，通过backtracking实现多层for循环
[17. Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)

都是不可放回的组合。每个number都还有两种情况，选或者不选，2的n次方组合。 然后卡一下数量（k）或者sum作为终止条件
[77. Combinations](https://leetcode.cn/problems/combinations/)
[216. Combination Sum III](https://leetcode.com/problems/combination-sum-iii/) 
[40. Combination Sum II](https://leetcode.com/problems/combination-sum-ii/)  唯一不同是，本身candidate有重复，结果的组合又不能重复，因此要先排序，方便处理重复
[90. Subsets II](https://leetcode.com/problems/subsets-ii/)  除了结束条件，其他和40题完全一样，包括处理重复的方式
[78. Subsets](https://leetcode.com/problems/subsets/)

可放回。但是只看组合，排列不同算相同。  因此backtracking的每一次调用，for循环顺序顺序枚举一遍
[39. Combination Sum](https://leetcode.cn/problems/combination-sum/)

## 2.2 DFS
[437. Path Sum III](https://leetcode.com/problems/path-sum-iii/)

## 2.3 BFS
### 2.3.1 BFS
1.   Word Ladder
2.   Word Ladder II
3.   Open the Lock
4.   Race Car
5. 
### 2.3.2 BFS Matrix
1.   01 Matrix
2.   Cut Off Trees for Golf Event
3.   Shortest Bridge

### 2.3.3 BFS Map
[127. Word Ladder](https://leetcode.com/problems/word-ladder/submissions/)


## other
1.  Permutations
2.  Permutations II
3.   Letter Case Permutation

## Partition（划分子集、子序列等）
1.   Partition to K Equal Sum Subsets
2.  Restore IP Addresses
3.   Palindrome Partitioning


## 图论
[996. Number of Squareful Arrays](https://leetcode.com/problems/number-of-squareful-arrays/)
