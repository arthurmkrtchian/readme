# Performance

The performance of various longhmap methods has been tested under different load scenarios. 

The benchmarking was conducted using datasets of varying sizes:

20,000,000 elements
10,000,000 elements
5,000,000 elements
2,500,000 elements

In the table below displays:
1. How fast the methods work in theory (referred to as "Complexity").
2. The actual time they took (ms).

## Performance Analysis of array-based LongMap Methods

| **Method**               | **Avg. Complexity** | **for 20 mln elements** | **10 mln** | **5 mln** | **2.5 mln** |
|--------------------------|---------------------|-------------------------|------------|-----------|-------------|
| `put(long key, V value)` | **O(n)**            | 1515,11                 | 668,45     | 229,40    | 94,83       | 
| `get(long key)`          | **O(1)**            | 0,07 	                 | 0,06       | 0,05      | 0,05        |
| `remove(long key)`       | **O(1)**            | 0,06                    | 0,05       | 0,03      | 0,03        |
| `isEmpty()`              | **O(1)**            | 0,05 	                 | 0,04 	    | 0,02 	    | 0,03        |
| `containsKey(long key)`  | **O(1)**            | 0,08 	                 | 0,05       | 0,03 	    | 0,03        |
| `containsValue(V value)` | **O(1)**            | 0,07 	                 | 0,05 	    | 0,03      | 0,03        |
| `keys()`                 | **O(n)**            | 353,53 	               | 82,92      | 33,10     | 18,45       |
| `values()`               | **O(n)**            | 488,96 	               | 138,38     | 78,45     | 32,42       |
| `size()`                 | **O(1)**            | 0,07                    | 0,05       | 0,03 	    | 0,03        |
| `clear()`                | **O(1)**            | 0,05                    | 0,04       | 0,03      | 0,03        |


## Performance Analysis of arrayList-based LongMap Methods

| **Method**               | **Avg. Complexity** | **for 20 mln elements** | **10 mln** | **5 mln** | **2.5 mln** |
|--------------------------|---------------------|-------------------------|------------|-----------|-------------|
| `put(long key, V value)` | **O(n)**            | 2233.64                 | 1224.53    | 424.92    | 232.37      | 
| `get(long key)`          | **O(1)**            | 1.30 	                 | 1.16       | 0.08      | 0.06        |
| `remove(long key)`       | **O(1)**            | 0.32                    | 0.14       | 0.48      | 0.08        |
| `isEmpty()`              | **O(1)**            | 0.19 	                 | 0.12 	    | 0.06 	    | 0.05        |
| `containsKey(long key)`  | **O(1)**            | 0.35 	                 | 0.13       | 0.06 	    | 0.05        |
| `containsValue(V value)` | **O(1)**            | 0.26 	                 | 0.15 	    | 0.06      | 0.05        |
| `keys()`                 | **O(n)**            | 426.61 	               | 155.40     | 73.76     | 29.30       |
| `values()`               | **O(n)**            | 676.70 	               | 366.33     | 199.70    | 82.86       |
| `size()`                 | **O(1)**            | 0.31                    | 0.10       | 0.08 	    | 0.06        |
| `clear()`                | **O(n)**            | 43.53                   | 35.85      | 12.01     | 3.68        |


Despite the increased runtime of the methods `get(long key)`, `remove(long key)`, `isEmpty()`, `containsKey(long key)`, and `containsValue(V value)` under various loads, their maximum execution time does not exceed 2 ms. For this reason, they are assigned a complexity of **O(1)**. The same situation arises when testing the standard **HashMap**.

When comparing the two implementations using **Array** and **ArrayList**, it's evident that the difference in execution time can reach up to **68%** in favor of the array implementation, especially in the case of the values() method.


### Testing Environment Specifications:

The following tests were conducted on this machine:

- **OS**: Ubuntu Jammy Jellyfish (LTS)
- **Kernel**: 5.15
- **CPU**: Core i5-6200U (2.3 - 2.8 GHz)
- **Core Quantity**: Dual-Core
- **GPU**: Nvidia GeForce 940MX
- **Storage**: 512GB SSD
- **RAM**: 16GB 2133Mhz
