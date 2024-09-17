Median of Two Sorted Arrays of Different Size in Python
Here, on this page, we will discuss the program to find the Median of Two Sorted Arrays of Different Size in Python programming language. We are given two sorted arrays say a[ ] and b[ ] of size n and m respectively. We need to find the median of these two sorted arrays.

Python Program to Find Median of Two Sorted Arrays of Different Size

Algorithm
After merging both arrays and sorting them send it to the function to find median
If the length of the array is even then find the floor value of l divided by 2 and store it in medium
Set median equals to sum of (array[medium] and array[medium-1]) divided by 2
return median
Else set medium equals to ceil(l/2) and return array[medium -1]
Median of 2 sorted arrays of different size in Python
Python Code
Run
from math import ceil


def median_of_two_arrays(len, array):
    if (len % 2) == 0:
        medium = len // 2
        median = (array[medium] + array[medium - 1]) / 2
        return median
    else:
        medium = ceil(len / 2)
        return array[medium - 1]


array1 = [2, 10, 12, 26]
array2 = [3, 6, 30, 78, 90]
print("After merging and sorting both array : ", end="")
array1 += array2
array1.sort()
print(array1)
ans = median_of_two_arrays(len(array1), array1)
print("Median :", ans)
Output
After merging and sorting both array : [2, 3, 6, 10, 12, 26, 30, 78, 90]
Median : 12
