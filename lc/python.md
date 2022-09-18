# Python3

## 常用数据结构
参考：https://realpython.com/python-data-structures/#queuepriorityqueue-beautiful-priority-queues

1. dict
```python
### defaultdict
# 可以为所有key设定默认值。默认值可以是任何可以初始化的类。 一旦key被访问，key对应的默认值就被设定
from collections import defaultdict 

>> a = defaultdict(list)
>> a["test"]
>> a

{"test": []}

### Counter
# 可以在dict的基础上，方便统计数量，以及most_common（众数）等
from collections import Counter

# 初始化：iterable or mapping
>>> c = Counter('gallahad')                 # a new counter from an iterable
>>> c = Counter({'red': 4, 'blue': 2})      # a new counter from a mapping

# 众数
>>> Counter('abracadabra').most_common(3)
[('a', 5), ('b', 2), ('r', 2)]

# 减法、总和等等
subtract()
total()

```

```

# stack
list
from collections import deque

# 堆/优先队列
from queue import PriorityQueue
    # compare是按照sorted实现的，因此插入元素要可对比。当不可对比时，参考如下。  实现包含__lt__, __eq__方法的类
    # https://stackoverflow.com/questions/57487170/is-it-possible-to-pass-a-comparator-to-a-priorityqueue-in-python
import heapq
```


## 常用技巧

```python
### 初始化
c = {'a': 1, 'b': 2}
{x: [] for x in c} # init dict using for loop

### 数组item交换：
a[i], a[j] = a[j], a[i]

### str to char array
a = '123'
b = list(a)

### range is xrange in python2

### lowcase letter，uppercase letter，digits。https://docs.python.org/3.5/library/string.html
string.ascii_lowercase
string.ascii_uppercase
string.digits
string.ascii_letters # string.ascii_lowercase + string.ascii_uppercase

### assignment, copy and deepcopy
# In python everything is a reference. Nothing gets copied unless you explicitly copy it.
# https://stackoverflow.com/questions/42032384/in-python-is-a-function-return-a-shallow-or-deep-copy
# https://towardsdatascience.com/assignment-shallow-or-deep-a-story-about-pythons-memory-management-b8fad87bfa6c

### scope
# local、enclosing、global、built-in
# https://realpython.com/python-scope-legb-rule/
```
