![image](https://github.com/user-attachments/assets/57e6590d-75ed-47d3-afee-219471c73970)# Linear Search and Binary search
## AIM:
To write a program to perform linear search and binary search using python programming.
## EQUIPMENTS REQUIRED:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## ALGORITHM:
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
## PROGRAM:
i)	#Use a linear search method to match the item in a list.
```
#Program for linear search method to match the item in a list
#Developed by:Daksha Subbaian
#RegisterNumber:212223230036

def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k = eval(input())
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by:Daksha Subbaian
#RegisterNumber:212223230036

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
        
array=eval(input())
array.sort()
k=eval(input())

result=binarySearchIter(array,k,0,len(array)-1)
if (result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
#Program to find the element in a list using Binary Search (recursive Method).
#Developed by:Daksha Subbaian
#RegisterNumber:212223230036 

def binarySearch(arr, k, low, high):
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
           return mid
        elif array[mid]<k:
            low=mid+1
            return binarySearch(array,k,low,high)
        else:
            high=mid-1
            return binarySearch(array,k,low,high)
    else:
        return -1
        
array=eval(input())
array.sort()
print(array)
k=eval(input())
n=len(array)
t=binarySearch(array,k,0,n-1)
if t==-1:
    print("Element not found")
else:
    print("Element found at index: ",t)
```
## SAMPLE INPUT AND OUTPUT:
![image](https://github.com/user-attachments/assets/a4916102-58de-4f9a-a489-c47927dc4ce2)
![image](https://github.com/user-attachments/assets/4568850c-f758-4a91-a367-e370a2120770)
![image](https://github.com/user-attachments/assets/0ba7a7a5-7a85-4332-aa85-59acdbd0db51)




## RESULT:
Thus the linear search and binary search algorithm is implemented using python programming.
