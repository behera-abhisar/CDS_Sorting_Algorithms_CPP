# EXPERIMENT 21: SORTING ALGORITHMS IN C++

## AIM
To implement and understand the working of various sorting algorithms including **Selection Sort**, **Bubble Sort**, and **Quick Sort**, and to analyze their efficiency in arranging elements in ascending order.

## TOOLS REQUIRED
- Computer with C++ compiler (GCC/CodeBlocks/Visual Studio Code)  
- Basic knowledge of C++ programming  
- Text editor or IDE for coding  

## THEORY
Sorting is the process of arranging data in a particular order, typically ascending or descending. It is one of the fundamental operations in computer science, used for optimizing searching, organizing data, and improving readability.

### Key Sorting Algorithms

1. **Selection Sort**
   - Works by repeatedly finding the minimum element from the unsorted part and putting it at the beginning.
   - **Time Complexity:** O(n²) for worst, average, and best cases.
   - **Space Complexity:** O(1) (In-place sorting).
   - Suitable for small datasets or educational purposes.

2. **Bubble Sort**
   - Repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.
   - Largest elements "bubble" to the end in each pass.
   - **Time Complexity:** O(n²) in worst and average cases, O(n) in best case (already sorted).
   - **Space Complexity:** O(1), in-place.

3. **Quick Sort**
   - A divide-and-conquer algorithm that selects a "pivot" element and partitions the array around the pivot.
   - Recursively sorts the partitions.
   - **Time Complexity:** O(n log n) on average, O(n²) in worst case (if pivot selection is poor).
   - **Space Complexity:** O(log n) due to recursion stack.
   - Highly efficient for large datasets.

### Advantages of Sorting
- Speeds up searching operations.
- Makes data more readable and structured.
- Essential for efficient algorithm design in higher-level operations like merging, searching, and optimization.

### Practical Use
Sorting algorithms are widely used in databases, file systems, data processing, and whenever ordered data is required for operations like searching or reporting.

## EXPERIMENT 21(A): SELECTION SORT IN C++

### ALGORITHM
1. **START**  
2. Initialize an array `arr[]` of size `n`.  
3. For each index `i` from 0 to `n-2`:  
   - Assume `minIndex = i`.  
   - For each index `j` from `i+1` to `n-1`:  
     - If `arr[j] < arr[minIndex]`, update `minIndex = j`.  
   - Swap `arr[i]` and `arr[minIndex]`.  
4. Repeat until the array is completely sorted.  
5. Display the sorted array.  
6. **STOP**

## EXPERIMENT 21(B): BUBBLE SORT IN C++

### ALGORITHM
1. **START**  
2. Initialize an array `arr[]` of size `n`.  
3. For each index `i` from 0 to `n-2`:  
   - Set a boolean `swap = false`.  
   - For each index `j` from 0 to `n-i-2`:  
     - If `arr[j] > arr[j+1]`, swap `arr[j]` and `arr[j+1]` and set `swap = true`.  
   - If no swaps occurred (`swap == false`), break the loop early.  
4. Repeat until the array is completely sorted.  
5. Display the sorted array.  
6. **STOP**

## EXPERIMENT 21(C): QUICK SORT IN C++

### ALGORITHM
1. **START**  
2. Initialize an array `arr[]` of size `n`.  
3. Define a `partition(arr, low, high)` function:  
   - Choose `arr[high]` as the pivot.  
   - Initialize `i = low - 1`.  
   - For each `j` from `low` to `high-1`:  
     - If `arr[j] < pivot`, increment `i` and swap `arr[i]` with `arr[j]`.  
   - Swap `arr[i+1]` with `arr[high]` and return `i+1` as partition index.  
4. Define `quickSort(arr, low, high)` function:  
   - If `low < high`:  
     - Call `partition()` to get `pi`.  
     - Recursively call `quickSort(arr, low, pi-1)` and `quickSort(arr, pi+1, high)`.  
5. Call `quickSort(arr, 0, n-1)` to sort the array.  
6. Display the sorted array.  
7. **STOP**

## CONCLUSION

In this experiment, we implemented and studied three sorting algorithms: **Selection Sort**, **Bubble Sort**, and **Quick Sort**. We observed the differences in their working mechanisms, efficiency, and time complexity. Quick Sort proved to be the fastest among them for larger datasets due to its **divide-and-conquer approach**, while Bubble and Selection Sorts are simpler but less efficient for large arrays. This experiment helped reinforce understanding of array manipulation, algorithm design, and recursive problem-solving in C++.
