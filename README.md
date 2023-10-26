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
2. The actual time they took (ms).


| **Method**               | **Avg. Complexity** | **for 20 mln elements** | **10 mln** | **5 mln** | **2.5 mln** |
|--------------------------|---------------------|-------------------------|------------|-----------|-------------|
| `put(long key, V value)` |**O(n)**             | 2048.42                 | 983.99     | 386.28    | 208.69      | 
| `get(long key)`          | **O(n)**            | 1.27 	                 | 0.43       | 0.10      | 0.07        |
| `remove(long key)`       | **O(1)**            | 1.53                    | 0.31       | 0.14      | 0.11        |
| `isEmpty()`              | **O(1)**            | 0.23 	                 | 0.09 	    | 0.05 	    | 0.04        |
| `containsKey(long key)`  | **O(1)**            | 0.19 	                 | 0.18       | 0.06 	    | 0.05        |
| `containsValue(V value)` | **O(1)**            | 0.25 	                 | 0.12 	    | 0.05      | 0.05        |
| `keys()`                 | **O(n)**            | 378.35 	               | 201.72     | 51.89     | 22.39       |
| `values()`               | **O(n)**            | 401.07 	               | 255.61     | 94.49     | 46.05       |
| `size()`                 | **O(1)**            | 0.28                    | 0.58       | 0.06 	    | 0.06        |
| `clear()`                | **O(n)**            | 17.02                   | 17.57      | 386.28    | 3.04        |
