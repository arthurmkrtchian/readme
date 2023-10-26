# Performance

## Performance Analysis of array-based LongMap Methods

The performance of various longhmap methods has been rigorously tested under different load scenarios. 

The benchmarking was conducted using datasets of varying sizes:

20,000,000 elements
10,000,000 elements
5,000,000 elements
2,500,000 elements

In the table below displays:
1. How fast the methods work in theory (referred to as "Complexity").
2. The actual time they took with 20,000,000 items.


| **Method**               | **Average Complexity**| **Average latency for 20 mln elements**|
|--------------------------|-----------------------|----------------------|
| `put(long key, V value)` | O(n)                  | 2622.77 ms	          |
| `get(long key)`          | O(1)                  | 0.10 ms	            |
| `remove(long key)`       | O(1)                  | 0.14 ms              |
| `isEmpty()`              | O(1)                  | 0.13 ms	            |
| `containsKey(long key)`  | O(1)                  | 0.29 ms	            |
| `containsValue(V value)` | O(1)                  | 0.23 ms	            |
| `keys()`                 | O(n log n)            | 389.43 ms	          |
| `values()`               | O(n log n)            | 636.76 ms	          |
| `size()`                 | O(1)                  | 0.28 ms              |
| `clear()`                | O(n)                  | 17.35 ms             |
