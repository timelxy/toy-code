
## how to understand

1. construct

```python
# nums: 原始数组
# i是原始数组index + 1
# v = nums[i - 1]

while i <= n:
    BITTree[i] += v
    i += i & (-i) # 不断的从右向左移动least significant binary 1

```
for example, i = 76(1001100), nums[i - 1] ought to be added in:
- 80 ( 1010000)
- 96 ( 1100000)
- 128(10000000)
- ...



3. getPrefixSum

```python
ret = 0
while i > 0:
    ret += BITTree[i]
    i -= i & (-i)
    
return ret
```
