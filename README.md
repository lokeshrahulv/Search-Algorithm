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

Program for linear search method to match the item in a list
Developed by:LOKESH RAHUL V V 
RegisterNumber: 22004702

def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
k = eval(input())
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

Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:LOKESH RAHUL V V
RegisterNumber: 22004702

def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
array = eval(input())
array.sort()
k = eval(input())
result=binarySearchIter(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

Program to find the element in a list using Binary Search (recursive Method).
Developed by: LOKESH RAHUL V V
RegisterNumber: 22004702

def binarySearch(arr, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return binarySearch(arr,k,low,mid-1)
        else:
            return binarySearch(arr,k,mid+1,high)
    return -1
    
array = eval(input())
array.sort()
k = eval(input()) 
result=binarySearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
## Sample Input and Output
i)![image](https://user-images.githubusercontent.com/118423842/213994377-327019cd-1078-4828-986b-3ab2015b1989.png)

ii)![image](https://user-images.githubusercontent.com/118423842/213994455-95347a41-38be-4e4a-bf25-2611460e138d.png)

iii)![image](https://user-images.githubusercontent.com/118423842/213994513-20c8b156-8569-4d74-b9a7-232130858bf5.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
