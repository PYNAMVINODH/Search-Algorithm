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
Developed by: PYNAM VINODH
RegisterNumber: 212223240131
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
    
array = eval(input())
# sort the array
array.sort()
n=len(array)
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
result = linearSearch(array,n,k)# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
if result==-1:
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
Developed by: PYNAM VINODH
RegisterNumber: 212223240131
'''

def BinarySearchIter(array, k, low, high):
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
result=BinarySearchIter(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
 


```
iii)	# Find the element in a list using Binary Search (recursive Method).
```

''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: PYNAM VINODH
RegisterNumber: 212223240131
'''
def BinarySearch(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(array,k,low,mid-1)
        else:
             return BinarySearch(array,k,mid+1,high)
    return -1
     
    
array = eval(input())
array.sort()
k = eval(input())  
result=BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)



```
## Sample Input and Output
i.Use a linear Search method to match the item in a list
![image](https://github.com/PYNAMVINODH/Search-Algorithm/assets/145742678/2b637e98-b9c3-4b2f-94f2-382bb064766e)

ii.Find the element in a list using Binarysearch(Iterative Method)
![image](https://github.com/PYNAMVINODH/Search-Algorithm/assets/145742678/4b75d9c4-cec9-4023-b3ec-a4c4dd37154d)

iii.Find the element in a list using BinarySearch (recursive Method)
![image](https://github.com/PYNAMVINODH/Search-Algorithm/assets/145742678/73893d60-b364-4335-be68-60204120eaff)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
