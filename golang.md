
# Queue

https://stackoverflow.com/questions/2818852/is-there-a-queue-implementation
上面的问题中已经讨论的很清楚了：

1. slice: 最简易的作为queue使用的方式，底层会有针对垃圾回收、内存重新分配等的优化。但是肯定还是有一定的memory waste
```go
// 1. slice
q := []int{}
q = append(q, 1) // append right
x = q[0] // left top
q = q[1:] // Discard top element
```

2. channels: From "The Go programming Language" by Donovan and Kernighan不推荐用channel，原文如下：
>Novices are sometimes tempted to use buffered channels within a single goroutine as a queue, lured by their pleas- ingly simple syntax, but this is a mistake. Channels are deeply connected to goroutine scheduling, and without another goroutine receiving from the channel, a sender—and perhaps the whole program—risks becoming blocked forever. If all you need is a simple queue, make one using a slice

3. ring buffer，需要自己实现，比较麻烦：https://github.com/gammazero/deque

