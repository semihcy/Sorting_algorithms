# Insertion_sort
Patika.dev Data Science course example

## Insertion Sort Algorithm

Insertion Sort works by dividing the list into two parts: the sorted part and the unsorted part. It repeatedly takes the next element from the unsorted part and inserts it into the correct position in the sorted part.

### Steps:
1. Start with the first element, considering it as sorted.
2. Take the next element and compare it with elements in the sorted part.
3. Shift all elements greater than the current element to the right.
4. Insert the current element into its correct position.
5. Repeat the process for all elements.

### Time Complexity:
- Best case: O(n) when the array is already sorted. We have to check all elements in the array. There are 'n' elements, so we perform 'n' checks. This means that there are n process.
- Worst case: O(n^2) when the array is sorted in reverse order. We compare n elements with other n elements. Since we compare n elements n times, the worst-case is n^2.

### Example:
[22,27,16,2,18,6] 
We apply insertion-sort to this array. We will compare all elements with each other in order. 
- [22,27,16,2,18,6] Compare 27 with 22. There is no problem. Keep going.
- [16,22,27,2,18,6] Compare 16 with 22 and 27. Move 16 to the zero index of the array.
- [2,16,22,27,18,6] Compare 2 with 16, 22 and 27. Move 2 to the zero index of the array.
- [2,16,18,22,27,6] Compare 18 with 2, 16, 22 and 27. Move 18 to the second index of the array.
- [2,6,16,18,22,27] Compare 6 with 2, 16, 18, 22, and 27. Move 6 to the first index of the array.

### Big-O Notation: 
Firstly, we compare the second element with the first element. So we do one process. When we compare other elements with previous elements, each time the number of processes increases by 1. 
1+2+3+.......+(n-1)+n=(n*(n+1))/2 => n^2/2 As a result Big-O is O(n^2).
  
If we try to find 18 in the array, we can find it in the average case due to the position in the array. 

## Selection Sort 
In short, we find the smallest element in the array each time and replace it with the first element.

### For Example:
[7,3,5,8,2,9,4,15,6]
1. [2,3,5,8,7,9,4,15,6] The smallest element is 2 and replace it with the first element.
2. [2,3,5,8,7,9,4,15,6] The smallest element is 3 it is already in the right position. NOTE:(When we replace the smallest element with the first element, the second element becomes the first element in the array.)
3. [2,3,4,8,7,9,5,15,6] The smallest element is 4 and replace it with 5.
4. [2,3,4,8,7,9,5,15,6] The smallest element is 5 and replace it with 8.


.
.
.
.
.


## Merge Sort
Merge Sort is one of the most popular sorting algorithms that is based on the principle of Divide and Conquer Algorithm.
Divide and Conqure --> Using the Divide and Conquer technique, we divide a problem into subproblems. When the solution to each subproblem is ready, we 'combine' the results from the subproblems to solve the main problem.

### For Example:
[16,21,11,8,12,22]
1. [16,21,11] [8,12,22] Divide the array by 2 until there is only one element left on all side.
2. [16] [21,11]  [8] [12,22]
3. [16] [21] [11]  [8] [12] [22]
4. [16] [11] [21]  [8] [12] [22]
5. [16] [11,21]  [8] [12,22]
6. [16,11,21] [8,12,22]
7. [8,11,12,16,21,22]

### Time Complexity:
Because of we divide the array with n elements by 2 each time, time complexity is 2^x=n => x=log(n) and since we apply this process to each element, Big-O is O(nlog(n)).


\## Binary Trees

Each node in a Binary Search Tree has at most two children, a left child and a right child, with the left child containing values less than the parent node and the right child containing values greater than the parent node.

\### For Example

\[7, 5, 1, 8, 3, 6, 0, 9, 4, 2\]

1\. \[7\] is the root node.

2\. \[5\] is less than \[7\] so move it to the left side of the root.

\[7\]

/

\[5\]

3\. \[1\] is less than \[7\] and also less than \[5\] so move it to the left side.

\[7\]

/

\[5\]

/

\[1\]

4\. \[8\] is greater than \[7\] so move it to the right side of the root.

\[7\]

/ \\

\[5\] \[8\]

/

\[1\]

5\. \[3\] is less than \[7\] and \[5\] so move it to the left side of these nodes but it is greater than \[1\] so move it to the right side of \[1\].

\[7\]

/ \\

\[5\] \[8\]

/

\[1\]

\\

\[3\]

6\. \[6\] is less than \[7\] but greater than \[5\] so move it to the right side of \[5\].

\[7\]

/ \\

\[5\] \[8\]

/ \\

\[1\] \[6\]

\\

\[3\]

7\. \[0\] is less than \[7\], \[5\] and \[1\] so move it to the left side of \[1\].

\[7\]

/ \\

\[5\] \[8\]

/ \\

\[1\] \[6\]

/ \\

\[0\] \[3\]

8\. \[9\] is greater than \[7\] and \[8\] so move it to the right side of \[8\].

\[7\]

/ \\

\[5\] \[8\]

/ \\ \\

\[1\] \[6\] \[9\]

/ \\

\[0\] \[3\]

9\. \[4\] is less than \[7\] and \[5\] but greater than \[1\] and \[3\] so move it to the right side of \[3\].

\[7\]

/ \\

\[5\] \[8\]

/ \\ \\

\[1\] \[6\] \[9\]

/ \\

\[0\] \[3\]

\\

\[4\]

10\. \[2\] is less than \[7\] and \[5\] but greater than \[1\] and it is less than \[3\] so move it to the left side of \[3\].

\[7\]

/ \\

\[5\] \[8\]

/ \\ \\

\[1\] \[6\] \[9\]

/ \\

\[0\] \[3\]

/ \\

\[2\] \[4\]




