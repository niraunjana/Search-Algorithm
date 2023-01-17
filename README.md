# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
Developed by: NIRAUNJANA GAYATHRI G R
RegisterNumber: 22008369
'''
def linearSearch(array,n,k):
    for i in range(0, n):
       if (array[i]==k):
           return i
    return-1
    
array = eval(input())
k=eval(input())
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: NIRAUNJANA GAYATHRI G R
RegisterNumber:  22008369
'''
def binarySearchIter(array, k, low, high):
    while low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] < k:
            low = mid + 1
        else:
            high = mid - 1
    return -1
array = eval(input())
array.sort()
k = eval(input()) 
result = binarySearchIter(array, k, 0, len(array)-1)
if(result == -1):
     print(array)
     print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: NIRAUNJANA GAYATHRI G R
RegisterNumber: 22008369
'''
def BinarySearch(arr, k, low, high):
    if high >= low:
        mid = low + (high - low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid] > k:
            return BinarySearch(arr, k, low, mid-1)
        else:
            return BinarySearch(arr, k, mid +1, high)
    else: 
        return-1
arr = eval(input())
arr.sort()
k = eval(input()) 
result = BinarySearch(arr, k, 0, len(arr)-1)
if(result == -1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ", result)







```
## Sample Input and Output:

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-37-51.png![image](https://user-images.githubusercontent.com/119395610/212870352-fbfe3d73-7940-46a4-a417-2dc3cab6fdbc.png)

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-38-03.png![image](https://user-images.githubusercontent.com/119395610/212870448-d51be700-b27c-49a7-8b19-1d8fab29db8e.png)

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-38-18.png![image](https://user-images.githubusercontent.com/119395610/212870862-f563ac89-27a3-492a-9ae2-ae1a0d5b64bd.png)

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-38-27.png![image](https://user-images.githubusercontent.com/119395610/212870929-b3b5e9bc-a6d1-436b-b16b-aa5bade9c38f.png)

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-39-19.png![image](https://user-images.githubusercontent.com/119395610/212870991-8dd2be2c-0476-4f5f-9f5a-5e1a1c99a7f8.png)

file:///home/sec/Pictures/Screenshots/Screenshot%20from%202023-01-17%2015-39-38.png![image](https://user-images.githubusercontent.com/119395610/212871084-1278a25b-3b4c-4b91-a11d-13c77e4d5554.png)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
