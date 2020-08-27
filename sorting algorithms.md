## Sorting Algorithms

**Contents**

- Bubble Sort
- Insertion Sort
- Merge Sort
- Quick Sort



### Bubble Sort

- Most **inefficient** approach - *Time Complexity - O(n)^2, Space Complexity O(1)*

- Compare array[0] and array[1] and swap if array[0] > array[1]
- This proceeds down the array (array[7] > array[8], True -> swap ex.)
- When it reaches of the first iteration, the last element of the array is sorted. The second iteration starts, and begins from array[0] again.

```python
def bubble_sort(array):
    
    # Optimization - If the rest of the list is swapped, stop traversing
	# the rest of the list
    
    swapped = True
    
    # Optimization 2 - Since last number is swapped, there is no need to
    # iterate to that number
    
    n = 0
    
    # traverse through the list n times, where n is the number of elements
    while swapped:
        swapped = False
        for i in range(len(array) - n - 1):
            if array[i] > array[i+1]:
                # swap
                array[i], array[i+1] = array[i+1], array[i]
                swapped = True
        n += 1
            
```

### Insertion Sort

W.I.P