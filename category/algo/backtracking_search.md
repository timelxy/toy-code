# knowledge
## Difference between backtracking and dfs
>backtracking handles an implicit tree and DFS deals with an explicit one. 
backtracking is DFS for implicit tree, while DFS is backtracking without pruning
-- https://stackoverflow.com/questions/1294720/whats-the-difference-between-backtracking-and-depth-first-search

# BFS主要方法
如何初始化bfs的queue？超级源点、排序等
如何不走重复的点？set记录走过的点的坐标
如何从当前点到adjacent点？queue、set都记录坐标

# Problem index
![](/lc/images/backtrack-search.png)


# problem category

## Combination，Subset
最简单的限定组合，通过backtracking实现多层for循环
[17. Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)

都是不可放回的组合。每个number都还有两种情况，选或者不选，2的n次方组合。 然后卡一下数量（k）或者sum作为终止条件
[77. Combinations](https://leetcode.cn/problems/combinations/)
[216. Combination Sum III](https://leetcode.com/problems/combination-sum-iii/) 
[40. Combination Sum II](https://leetcode.com/problems/combination-sum-ii/)  唯一不同是，本身candidate有重复，结果的组合又不能重复，因此要先排序，方便处理重复
[78. Subsets](https://leetcode.com/problems/subsets/)

可放回。但是只看组合，排列不同算相同。  因此backtracking的每一次调用，for循环顺序顺序枚举一遍
[39. Combination Sum](https://leetcode.cn/problems/combination-sum/)

permutation，和上面都不太一样
[377. Combination Sum IV](https://leetcode.com/problems/combination-sum-iv/)


90. Subsets II

## Permutation
46. Permutations
47. Permutations II
784. Letter Case Permutation

## Partition（划分子集、子序列等）
698. Partition to K Equal Sum Subsets
93. Restore IP Addresses
131. Palindrome Partitioning

## DFS
[437. Path Sum III](https://leetcode.com/problems/path-sum-iii/)

## BFS（Matrix）
542. 01 Matrix
675. Cut Off Trees for Golf Event
934. Shortest Bridge



## BFS
127. Word Ladder
126. Word Ladder II
752. Open the Lock
818. Race Car


## 图论
[996. Number of Squareful Arrays](https://leetcode.com/problems/number-of-squareful-arrays/)
