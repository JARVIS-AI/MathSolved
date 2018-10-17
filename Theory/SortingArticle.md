### Sorting Algorithms

**Note :** This article is made by Jarvis-AI (Amir Mohammad Safari) and His friend Nyauki Magical Girl. From IRAN & CANADA together. Inspired By Nyauki Sort Java 
PR.

Jarvis Mercer also made her code in native macOS App 😎

Both are great in their work and they are friend.
Generally this article is under MIT License and Accepted for Publishing by saying Sources. If NOT then don't Copy and Get Permission from us.

### License

```C++
/*
* Copyright (c) Project Nayuki and Jarvis-AI
 * https://www.nayuki.io/page/sorting-algorithms-demo-java | git: Jarvis-ai/sortingAlgos
 *
 * (MIT License)
 * Permission is hereby granted, free of charge, to any person obtaining a copy of
 * this software and associated documentation files (the "Software"), to deal in
 * the Software without restriction, including without limitation the rights to
 * use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
 * the Software, and to permit persons to whom the Software is furnished to do so,
 * subject to the following conditions:
 * - The above copyright notice and this permission notice shall be included in
 *   all copies or substantial portions of the Software.
 * - The Software is provided "as is", without warranty of any kind, express or
 *   implied, including but not limited to the warranties of merchantability,
 *   fitness for a particular purpose and noninfringement. In no event shall the
 *   authors or copyright holders be liable for any claim, damages or other
 *   liability, whether in an action of contract, tort or otherwise, arising from,
 *   out of or in connection with the Software or the use or other dealings in the
 *   Software.
 */
```

We just show some of sort algorithm codes, there is lot's of sorting algorithm out there most of them will be teached during science stuff and academic university periods and some of them are complicated others easy, this is nature of mathmatics and science.

So if you don't unerstand what is the algorithm of that souce code or any other algorithm sorting in mathmatics just study and practice by solve it even if you shoud try more than 100 times.

Get helps and watch the masters confrences. Study books and practice math.

It helps much.

#### **Bubble Sort**

Sort Algorithm complexity in Math (best case)  : $$O(N^2)$$

Bubble sort is one the sorting algorithm that its complex $$O(N)$$ .
In this situation it has uses array unsorted list and doing sorting.
Bubble sort has got 2 Faces of way.

1. Without FLAG
2. With FLAG

The first one has a problem that is when we give this algorithm a sorted array. Bubble again doing sorting things.
But in the second, When we give it a sorted array it has DONE with it.
Means not again sorting the sorted array.

> JAVA Code | Bubble Sort

```java
// Optimized java implementation 
// of Bubble sort 
import java.io.*; 

class GFG 
{ 
	// An optimized version of Bubble Sort 
	static void bubbleSort(int arr[], int n) 
	{ 
		int i, j, temp; 
		boolean swapped; 
		for (i = 0; i < n - 1; i++) 
		{ 
			swapped = false; 
			for (j = 0; j < n - i - 1; j++) 
			{ 
				if (arr[j] > arr[j + 1]) 
				{ 
					// swap arr[j] and arr[j+1] 
					temp = arr[j]; 
					arr[j] = arr[j + 1]; 
					arr[j + 1] = temp; 
					swapped = true; 
				} 
			} 

			// IF no two elements were 
			// swapped by inner loop, then break 
			if (swapped == false) 
				break; 
		} 
	} 

	// Function to print an array 
	static void printArray(int arr[], int size) 
	{ 
		int i; 
		for (i = 0; i < size; i++) 
			System.out.print(arr[i] + " "); 
		System.out.println(); 
	} 

	// Driver program 
	public static void main(String args[]) 
	{ 
		int arr[] = { 64, 34, 25, 12, 22, 11, 90 }; 
		int n = arr.length; 
		bubbleSort(arr, n); 
		System.out.println("Sorted array: "); 
		printArray(arr, n); 
	} 
} 


// This code is contributed 
// by Nikita Tiwari. 

```

> C Code | Bubble Sort

```C
// C program for implementation of Bubble sort 
#include <stdio.h> 

void swap(int *xp, int *yp) 
{ 
	int temp = *xp; 
	*xp = *yp; 
	*yp = temp; 
} 

// A function to implement bubble sort 
void bubbleSort(int arr[], int n) 
{ 
int i, j; 
for (i = 0; i < n-1; i++)	 

	// Last i elements are already in place 
	for (j = 0; j < n-i-1; j++) 
		if (arr[j] > arr[j+1]) 
			swap(&arr[j], &arr[j+1]); 
} 

/* Function to print an array */
void printArray(int arr[], int size) 
{ 
	int i; 
	for (i=0; i < size; i++) 
		printf("%d ", arr[i]); 
	printf("n"); 
} 

// Driver program to test above functions 
int main() 
{ 
	int arr[] = {64, 34, 25, 12, 22, 11, 90}; 
	int n = sizeof(arr)/sizeof(arr[0]); 
	bubbleSort(arr, n); 
	printf("Sorted array: \n"); 
	printArray(arr, n); 
	return 0; 
} 

```

> C++ Code | Bubble Sort

```C++
// Optimized implementation of Bubble sort 
#include <stdio.h> 

void swap(int *xp, int *yp) 
{ 
	int temp = *xp; 
	*xp = *yp; 
	*yp = temp; 
} 

// An optimized version of Bubble Sort 
void bubbleSort(int arr[], int n) 
{ 
int i, j; 
bool swapped; 
for (i = 0; i < n-1; i++) 
{ 
	swapped = false; 
	for (j = 0; j < n-i-1; j++) 
	{ 
		if (arr[j] > arr[j+1]) 
		{ 
		swap(&arr[j], &arr[j+1]); 
		swapped = true; 
		} 
	} 

	// IF no two elements were swapped by inner loop, then break 
	if (swapped == false) 
		break; 
} 
} 

/* Function to print an array */
void printArray(int arr[], int size) 
{ 
	int i; 
	for (i=0; i < size; i++) 
		printf("%d ", arr[i]); 
	printf("n"); 
} 

// Driver program to test above functions 
int main() 
{ 
	int arr[] = {64, 34, 25, 12, 22, 11, 90}; 
	int n = sizeof(arr)/sizeof(arr[0]); 
	bubbleSort(arr, n); 
	printf("Sorted array: \n"); 
	printArray(arr, n); 
	return 0; 
} 

```

> Python Code | Bubble Sort


```python
# Python3 Optimized implementation 
# of Bubble sort 

# An optimized version of Bubble Sort 
def bubbleSort(arr): 
	n = len(arr) 

	# Traverse through all array elements 
	for i in range(n): 
		swapped = False

		# Last i elements are already 
		# in place 
		for j in range(0, n-i-1): 

			# traverse the array from 0 to 
			# n-i-1. Swap if the element 
			# found is greater than the 
			# next element 
			if arr[j] > arr[j+1] : 
				arr[j], arr[j+1] = arr[j+1], arr[j] 
				swapped = True

		# IF no two elements were swapped 
		# by inner loop, then break 
		if swapped == False: 
			break
		
# Driver code to test above 
arr = [64, 34, 25, 12, 22, 11, 90] 

bubbleSort(arr) 

print ("Sorted array :") 
for i in range(len(arr)): 
	print ("%d" %arr[i],end=" ") 

# This code is contributed by Shreyanshi Arun 

```

> Shell Code | Bubble Sort


```shell
# Sorting the array in Bash 
# using Bubble sort 

# Static input of Array 
arr = (10 8 20 100 12) 

echo "Array in original order"
echo ${arr[*]} 

# Performing Bubble sort 
for ((i = 0; i<5; i++)) 
do
	
	for((j = i; j<5-i-1; j++)) 
	do
	
		if ((${arr[j]} > ${arr[$((j+1))]})) 
		then
			# swap 
			temp = ${arr[$j]} 
			arr[$j] = ${arr[$((j+1))]} 
			arr[$((j+1))] = $temp 
		fi
	done
done

echo "Array in sorted order :"
echo ${arr[*]} 

```



#### **Selection Sort**

Sort Algorithm complexity in math (Best case)  : $$O(N^2)$$

Worst case : $$O(1)$$

> C Code

```c
// C program for implementation of selection sort 
#include <stdio.h> 

void swap(int *xp, int *yp) 
{ 
	int temp = *xp; 
	*xp = *yp; 
	*yp = temp; 
} 

void selectionSort(int arr[], int n) 
{ 
	int i, j, min_idx; 

	// One by one move boundary of unsorted subarray 
	for (i = 0; i < n-1; i++) 
	{ 
		// Find the minimum element in unsorted array 
		min_idx = i; 
		for (j = i+1; j < n; j++) 
		if (arr[j] < arr[min_idx]) 
			min_idx = j; 

		// Swap the found minimum element with the first element 
		swap(&arr[min_idx], &arr[i]); 
	} 
} 

/* Function to print an array */
void printArray(int arr[], int size) 
{ 
	int i; 
	for (i=0; i < size; i++) 
		printf("%d ", arr[i]); 
	printf("\n"); 
} 

// Driver program to test above functions 
int main() 
{ 
	int arr[] = {64, 25, 12, 22, 11}; 
	int n = sizeof(arr)/sizeof(arr[0]); 
	selectionSort(arr, n); 
	printf("Sorted array: \n"); 
	printArray(arr, n); 
	return 0; 
} 

```

> Python Code

```python
# Python program for implementation of Selection 
# Sort 
import sys 
A = [64, 25, 12, 22, 11] 

# Traverse through all array elements 
for i in range(len(A)): 
	
	# Find the minimum element in remaining 
	# unsorted array 
	min_idx = i 
	for j in range(i+1, len(A)): 
		if A[min_idx] > A[j]: 
			min_idx = j 
			
	# Swap the found minimum element with 
	# the first element		 
	A[i], A[min_idx] = A[min_idx], A[i] 

# Driver code to test above 
print ("Sorted array") 
for i in range(len(A)): 
	print("%d" %A[i]), 

```

> Java Code

```java
// Java program for implementation of Selection Sort 
class SelectionSort 
{ 
	void sort(int arr[]) 
	{ 
		int n = arr.length; 

		// One by one move boundary of unsorted subarray 
		for (int i = 0; i < n-1; i++) 
		{ 
			// Find the minimum element in unsorted array 
			int min_idx = i; 
			for (int j = i+1; j < n; j++) 
				if (arr[j] < arr[min_idx]) 
					min_idx = j; 

			// Swap the found minimum element with the first 
			// element 
			int temp = arr[min_idx]; 
			arr[min_idx] = arr[i]; 
			arr[i] = temp; 
		} 
	} 

	// Prints the array 
	void printArray(int arr[]) 
	{ 
		int n = arr.length; 
		for (int i=0; i<n; ++i) 
			System.out.print(arr[i]+" "); 
		System.out.println(); 
	} 

	// Driver code to test above 
	public static void main(String args[]) 
	{ 
		SelectionSort ob = new SelectionSort(); 
		int arr[] = {64,25,12,22,11}; 
		ob.sort(arr); 
		System.out.println("Sorted array"); 
		ob.printArray(arr); 
	} 
} 
/* This code is contributed by Rajat Mishra*/

```



#### TimSort

> Sort Algorithm in Worst and Best Case : B ($$O(n log n)$$) - W ($$O(n)$$)

> C++ Code

```c++
// C++ program to perform TimSort. 
#include<bits/stdc++.h> 
using namespace std; 
const int RUN = 32; 

// this function sorts array from left index to 
// to right index which is of size atmost RUN 
void insertionSort(int arr[], int left, int right) 
{ 
	for (int i = left + 1; i <= right; i++) 
	{ 
		int temp = arr[i]; 
		int j = i - 1; 
		while (arr[j] > temp && j >= left) 
		{ 
			arr[j+1] = arr[j]; 
			j--; 
		} 
		arr[j+1] = temp; 
	} 
} 

// merge function merges the sorted runs 
void merge(int arr[], int l, int m, int r) 
{ 
	// original array is broken in two parts 
	// left and right array 
	int len1 = m - l + 1, len2 = r - m; 
	int left[len1], right[len2]; 
	for (int i = 0; i < len1; i++) 
		left[i] = arr[l + i]; 
	for (int i = 0; i < len2; i++) 
		right[i] = arr[m + 1 + i]; 

	int i = 0; 
	int j = 0; 
	int k = l; 

	// after comparing, we merge those two array 
	// in larger sub array 
	while (i < len1 && j < len2) 
	{ 
		if (left[i] <= right[j]) 
		{ 
			arr[k] = left[i]; 
			i++; 
		} 
		else
		{ 
			arr[k] = right[j]; 
			j++; 
		} 
		k++; 
	} 

	// copy remaining elements of left, if any 
	while (i < len1) 
	{ 
		arr[k] = left[i]; 
		k++; 
		i++; 
	} 

	// copy remaining element of right, if any 
	while (j < len2) 
	{ 
		arr[k] = right[j]; 
		k++; 
		j++; 
	} 
} 

// iterative Timsort function to sort the 
// array[0...n-1] (similar to merge sort) 
void timSort(int arr[], int n) 
{ 
	// Sort individual subarrays of size RUN 
	for (int i = 0; i < n; i+=RUN) 
		insertionSort(arr, i, min((i+31), (n-1))); 

	// start merging from size RUN (or 32). It will merge 
	// to form size 64, then 128, 256 and so on .... 
	for (int size = RUN; size < n; size = 2*size) 
	{ 
		// pick starting point of left sub array. We 
		// are going to merge arr[left..left+size-1] 
		// and arr[left+size, left+2*size-1] 
		// After every merge, we increase left by 2*size 
		for (int left = 0; left < n; left += 2*size) 
		{ 
			// find ending point of left sub array 
			// mid+1 is starting point of right sub array 
			int mid = left + size - 1; 
			int right = min((left + 2*size - 1), (n-1)); 

			// merge sub array arr[left.....mid] & 
			// arr[mid+1....right] 
			merge(arr, left, mid, right); 
		} 
	} 
} 

// utility function to print the Array 
void printArray(int arr[], int n) 
{ 
	for (int i = 0; i < n; i++) 
		printf("%d ", arr[i]); 
	printf("\n"); 
} 

// Driver program to test above function 
int main() 
{ 
	int arr[] = {5, 21, 7, 23, 19}; 
	int n = sizeof(arr)/sizeof(arr[0]); 
	printf("Given Array is\n"); 
	printArray(arr, n); 

	timSort(arr, n); 

	printf("After Sorting Array is\n"); 
	printArray(arr, n); 
	return 0; 
} 

```



> Python Code

```python
# based off of this code https://gist.github.com/nandajavarma/a3a6b62f34e74ec4c31674934327bbd3
# Brandon Skerritt
# https://skerritt.tech

def binary_search(the_array, item, start, end):
    if start == end:
        if the_array[start] > item:
            return start
        else:
            return start + 1
    if start > end:
        return start

    mid = round((start + end)/ 2)

    if the_array[mid] < item:
        return binary_search(the_array, item, mid + 1, end)

    elif the_array[mid] > item:
        return binary_search(the_array, item, start, mid - 1)

    else:
        return mid

"""
Insertion sort that timsort uses if the array size is small or if
the size of the "run" is small
"""
def insertion_sort(the_array):
    l = len(the_array)
    for index in range(1, l):
        value = the_array[index]
        pos = binary_search(the_array, value, 0, index - 1)
        the_array = the_array[:pos] + [value] + the_array[pos:index] + the_array[index+1:]
    return the_array

def merge(left, right):
    """Takes two sorted lists and returns a single sorted list by comparing the
    elements one at a time.
    [1, 2, 3, 4, 5, 6]
    """
    if not left:
        return right
    if not right:
        return left
    if left[0] < right[0]:
        return [left[0]] + merge(left[1:], right)
    return [right[0]] + merge(left, right[1:])

def timsort(the_array):
    runs, sorted_runs = [], []
    length = len(the_array)
    new_run = [the_array[0]]

    # for every i in the range of 1 to length of array
    for i in range(1, length):
        # if i is at the end of the list
        if i == length - 1:
            new_run.append(the_array[i])
            runs.append(new_run)
            break
        # if the i'th element of the array is less than the one before it
        if the_array[i] < the_array[i-1]:
            # if new_run is set to None (NULL)
            if not new_run:
                runs.append([the_array[i]])
                new_run.append(the_array[i])
            else:
                runs.append(new_run)
                new_run = []
        # else if its equal to or more than
        else:
            new_run.append(the_array[i])

    # for every item in runs, append it using insertion sort
    for item in runs:
        sorted_runs.append(insertion_sort(item))
    
    # for every run in sorted_runs, merge them
    sorted_array = []
    for run in sorted_runs:
        sorted_array = merge(sorted_array, run)

    print(sorted_array)

timsort([2, 3, 1, 5, 6, 7])
```



## License

Every code and samples are for their owner and writers, if you want to copy or using them in your work please caontac them.

Thanks

