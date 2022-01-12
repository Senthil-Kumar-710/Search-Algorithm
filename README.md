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
''' 
Program for linear search method to match the item in a list
Developed by: Senthil Kumar S
RegisterNumber: 21500410
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
array = eval(input())
array.sort()
print(array)
k = eval(input()) 
n=len(array)
result=linearSearch(array,n,k)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")



```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Senthil Kumar S
RegisterNumber: 21500410
'''
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid+1
    return -1
array=eval(input())
array.sort()
print(array)
k=eval(input()) 
low=0
high= len(array)-1
result=binarySearchIter(array, k, low, high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")






```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Senthil Kumar S
RegisterNumber: 21500410
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]<k:
            return BinarySearch(arr,k,mid+1,high)
        else:
            return BinarySearch(arr,k,low,mid+1)
    return -1
arr = eval(input())
arr.sort()
print(arr)
k = eval(input()) 
low=0
high=len(arr)-1
result=BinarySearch(arr, k, low, high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")




```
## Sample Input and Output

![list](https://user-images.githubusercontent.com/93860256/149075373-1f6d4229-bf58-46c8-baa1-8aaa3c53e54c.PNG)
![iter](https://user-images.githubusercontent.com/93860256/149075449-1e19e5ae-5451-41b0-9bf1-910ca1a2b48a.PNG)
![recur](https://user-images.githubusercontent.com/93860256/149075492-dada12e2-3b07-49eb-b533-2172f124b9aa.PNG)




## Output

![list output](https://user-images.githubusercontent.com/93860256/149075634-96b6c9dc-607b-4830-85d1-c24b61661a92.PNG)
![iter output](https://user-images.githubusercontent.com/93860256/149075732-1c15374c-f548-4a57-83eb-832b87d29dfd.PNG)
![recur output](https://user-images.githubusercontent.com/93860256/149075872-6e5cec2c-dd57-4f28-8ac8-631f12cb5a31.PNG)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.