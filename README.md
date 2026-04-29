
# Assignment 3: Sorting and Searching Algorithm Analysis

## Selected Algorithms

- Basic Sort: Bubble Sort
- Advanced Sort: Quick Sort
- Search: Binary Search

## Experiment Results

### Run 1

========== EXPERIMENTS ==========

ARRAY SIZE: 10
Basic sort: 7300 ns
Advanced sort: 8600 ns
Binary search: 3000 ns

ARRAY SIZE: 100
Basic sort: 211300 ns
Advanced sort: 28900 ns
Binary search: 1000 ns

ARRAY SIZE: 1000
Basic sort: 3787800 ns
Advanced sort: 225100 ns
Binary search: 1200 ns

========== TEST WITH SORTED DATA ==========
For already sorted array (size 1000):
Basic sort: 477300 ns
Advanced sort: 1167800 ns

### Run 2

========== EXPERIMENTS ==========

ARRAY SIZE: 10
Basic sort: 8600 ns
Advanced sort: 9900 ns
Binary search: 2900 ns

ARRAY SIZE: 100
Basic sort: 238200 ns
Advanced sort: 32400 ns
Binary search: 900 ns

ARRAY SIZE: 1000
Basic sort: 5029000 ns
Advanced sort: 307400 ns
Binary search: 1600 ns

========== TEST WITH SORTED DATA ==========
For already sorted array (size 1000):
Basic sort: 1980300 ns
Advanced sort: 1111000 ns

### Run 3

========== EXPERIMENTS ==========

ARRAY SIZE: 10
Basic sort: 8000 ns
Advanced sort: 11100 ns
Binary search: 3700 ns

ARRAY SIZE: 100
Basic sort: 217200 ns
Advanced sort: 30400 ns
Binary search: 1000 ns

ARRAY SIZE: 1000
Basic sort: 4241100 ns
Advanced sort: 299200 ns
Binary search: 1800 ns

========== TEST WITH SORTED DATA ==========
For already sorted array (size 1000):
Basic sort: 961500 ns
Advanced sort: 1513800 ns

## Performance Table (Run 1)

| Array Size | Bubble Sort (ns) | Quick Sort (ns) | Binary Search (ns) |
|------------|------------------|-----------------|---------------------|
| 10         | 7300             | 8600            | 3000                |
| 100        | 211300           | 28900           | 1000                |
| 1000       | 3787800          | 225100          | 1200                |

## Questions and Answers

1. Which sorting algorithm is faster? Why?

Quick Sort is faster on large arrays (100 and 1000 elements). On size 1000, Quick Sort took 225100 ns while Bubble Sort took 3787800 ns. On size 10, Bubble Sort was slightly faster due to overhead in Quick Sort's recursive calls.

2. How does performance change with input size?

Execution time increases as input size grows. Bubble Sort shows a quadratic increase. Quick Sort shows a slower, linearithmic increase. On size 1000, Bubble Sort is about 17 times slower than Quick Sort.

3. How does sorted vs unsorted data affect performance?

For Bubble Sort, sorted data is much faster (477300 ns vs 3787800 ns on size 1000). For Quick Sort, sorted data is slower (1167800 ns vs 225100 ns on size 1000) because Quick Sort picks the last element as pivot, which leads to worst-case performance on already sorted arrays.

4. Do the results match the expected Big-O complexity?

Yes. Bubble Sort (O(n²)) is significantly slower on large arrays. Quick Sort (O(n log n)) handles large arrays efficiently. Binary Search (O(log n)) runs almost instantly regardless of array size.

5. Which searching algorithm is more efficient? Why?

Binary Search is more efficient. It eliminates half of the remaining elements at each step (O(log n)), while Linear Search checks each element one by one (O(n)).

6. Why does Binary Search require a sorted array?

Binary Search compares the target value with the middle element. Based on whether the target is smaller or larger, it decides to search only the left or right half. This decision requires the array to be sorted.

## Reflection

I learned that Quick Sort is much faster than Bubble Sort on large arrays. On size 1000, Quick Sort took about 225100 ns while Bubble Sort took 3787800 ns. Binary Search is very fast at around 1000-3000 ns. The worst-case performance of Quick Sort on sorted arrays was interesting to observe.

## Screenshot

![results](<img width="1920" height="1080" alt="Снимок экрана 2026-04-30 013013" src="https://github.com/user-attachments/assets/fa429833-2bb5-4649-827e-3176ccbfbd24" />
)
