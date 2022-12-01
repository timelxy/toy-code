
# FIFO Queue
```go
// https://stackoverflow.com/questions/2818852/is-there-a-queue-implementation
// 1. slice
q := []int{}
q = append(q, 1) // append right
x = q[0] // left top
q = q[1:] // Discard top element
```

