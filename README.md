# List Operations and Searching in Python
This README file provides an explanation of the Python code that demonstrates various list operations, linear search, sorting, and searching in 2D lists.

## 1D List Operations
### Creating and Searching in 1D List
```python

myList = [10, 30, 5, 1, 2, 3]

def linearSearch(myList, target):
    for i in range(len(myList)):
        if myList[i] == target:
            return "Found"
    return "Not Found"

myList.sort()

print(myList)
print(linearSearch(myList, 30))
```
In this section, a 1D list myList is created and populated with integers. The linearSearch function is defined to search for a given target value in the list using a linear search algorithm. The list is then sorted using the built-in sort() function, and the sorted list is printed. The code then tests the linear search function by searching for the value 30 in the sorted list.

## 2D List Operations
### Creating and Searching in 2D List
```python

myList = [[9, 8, 7],
          [6, 5, 4],
          [3, 2, 1]]

def linearSearch(myList, target):
    for i in range(len(myList)):
        for j in range(len(myList[i])):
            if myList[i][j] == target:
                return "Found"
    return "Not Found"

print(linearSearch(myList, 5))

```
In this section, a 2D list myList is created with nested sublists. The linearSearch function is modified to perform a linear search for a target value in the 2D list. The code tests the linear search function by searching for the value 5 in the 2D list.

## Sorting a 2D List
```python

def sort2D(myList):
    myList1D = []
    for i in range(len(myList)):
        for j in range(len(myList[i])):
            myList1D.append(myList[i][j])
    myList1D.sort()

    sortedList = []
    k = 0
    for i in range(len(myList)):
        row = []
        for j in range(len(myList[i])):
            row.append(myList1D[k])
            k = k + 1
        sortedList.append(row)

    return sortedList

print(sort2D(myList))
```
This section defines the sort2D function that sorts a given 2D list. First, the elements of the 2D list are flattened into a 1D list, which is then sorted. The sorted 1D list is used to reconstruct the sorted 2D list. The code tests the sort2D function by sorting the previously defined myList and printing the sorted 2D list.

This README file provides an overview of the Python code's functionality, including creating, searching, and sorting 1D and 2D lists. It demonstrates the implementation of linear search and sorting algorithms for both list types.
