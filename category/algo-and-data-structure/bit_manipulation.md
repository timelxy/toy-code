## Knowledge
### 基本知识
1. 异或
- 基础知识
  - 任何数和 00 做异或运算，结果仍然是原来的数
  - 任何数和其自身做异或运算，结果是 0
  - 异或运算满足交换律和结合律
- 用法
  - 指定位取反。异或1
2. 其他组合用法
https://leetcode.com/problems/sum-of-two-integers/discuss/84278/A-summary%3A-how-to-use-bit-manipulation-to-solve-problems-easily-and-efficiently
- 最低位第一个1对应的数字
  - num & (-num)
  - num&~(num-1)
  - num^(num&(num-1))
- 最低位1设置为0（可用于循环处理二进制中的1位置）
  - num ^ (num & (-num))
  - num & (num - 1)。所谓的Brian Kernighan's Algorithm, https://iq.opengenus.org/brian-kernighan-algorithm/
- base ^ b ^ b = base; b ^ b = 0
- 不进位加法：用^进位：&

### 补码（two's complement）
https://zh.wikipedia.org/zh-sg/%E4%BA%8C%E8%A3%9C%E6%95%B8
1. 有符号数的常用底层二进制存储方式
2. 计算：-A的补码，等于(~A) + 1
3. 应用：减法、有符号数加法，都可以用补码加法代替
4. 溢出：高位溢出不影响计算结果
5. 实现：c++、java、python等的有符号数，底层二进制都是用补码实现的


### Python实现
整型没有位数限制，按照官方文档，理论上是无限存储（模拟来实现）

```python
# bin()方法，对于负数的返回结果，不是实际底层的二进制补码
>>> bin(8)
'0b1000'
>>> bin(-8) # 仅是对应正数二进制，加了符号
'-0b1000'

# 查看真实的负数二进制。参考：https://stackoverflow.com/questions/46044936/bitwise-and-between-negative-and-positive-numbers
# 可以看到，高位默认都是1，infinite个1
import math
def bin_format(integer):
    num_bytes = math.ceil(integer.bit_length()/8)  # Number required to represent value.
    ba = integer.to_bytes(num_bytes + 10, 'big', signed=integer<0) # 额外输出高位的1
    return ''.join('{:08b}'.format(b) for b in ba) + ' ({:4d})'.format(integer)
    
>>> bin_format(-8)
'1111111111111111111111111111111111111111111111111111111111111111111111111111111111111000 (  -8)'
```

### C++实现
c++的int是32位。有符号整型，如果溢出会报错。无符号不会

## Problems
37. Sudoku Solver 解法2
371. Sum of Two Integers
268. Missing Number
190. Reverse Bits
191. Number of 1 Bits
201. Bitwise AND of Numbers Range
187. Repeated DNA Sequences
136. Single Number
137. Single Number II
260. Single Number III
[78. Subsets](https://leetcode.com/problems/subsets/)     如何生成n位固定长度的二进制数？  见解法3
