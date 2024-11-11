# SEARCHING ALGORITHM
## NAME : Manas Shaileshbhai Dekivadia
## ID : 2023UCP1843
#
# DESCRIPTION
**Linear Search**
#
<ins>Definition</ins> :
>Assume that item is in an array in random order and we have to find an item. Then the only way to search for a target item is, to begin with, the first position and compare it to the target. If the item is at the same, we will return the position of the current item. Otherwise, we will move to the next position. If we arrive at the last position of an array and still can not find the target, we return -1. This is called the Linear search or Sequential search.[^1]
>
#
Time Complexity :  _O(n)_
#
Refrence Link : [Linear Search](https://www.geeksforgeeks.org/linear-search-vs-binary-search/).
![Linear Search Working](https://media.geeksforgeeks.org/wp-content/uploads/Linear.png)
Short Form : L<sup>s</sup>[^2]
#
ADVANTAGES:
- Simplicity: Linear search is easy to understand and implement.
- Works on unsorted data: Linear search can be used on both sorted and unsorted arrays.
#
DISADVANTAGES:
1. Time Complexity performance is directly proportional to the size of the dataset.
2. Linear search only provides basic search capabilities, such as searching for the first or last occurrence of a 
#
TASK
- [x] #Naive Searching
- [ ] Needs a lot of extra time
- [ ] Slowest Algorithm

> [!NOTE]  
> Please note this is the most slowest algorithm.

> [!TIP]
> If Anything is listed false please notify.

> [!IMPORTANT]
> Ensure that the data set is small while searching.

> [!WARNING]
> Large Data Set might require high time complexity.

> [!CAUTION]
> Memory Risk.
 
#
Algorithm:
```
#include <iostream>
using namespace std;
int search(int array[], int n, int x)
{

	// Going through array sequencially
	for (int i = 0; i < n; i++)
		if (array[i] == x)
			return i;
	return -1;
}
```
 

***Binary Search***
#
<ins>Definition</ins> :
>In a binary search, however, cut down your search to half as soon as you find the middle of a sorted list. The middle element is looked at to check if it is greater than or less than the value to be searched. Accordingly, a search is done to either half of the given list.[^1]
>
#
Time Complexity : ~~O(n)~~   _O(logn)_
#
Refrence Link : [Binary Search](https://www.geeksforgeeks.org/linear-search-vs-binary-search/).
![Linear Search Working](https://media.geeksforgeeks.org/wp-content/uploads/binary-3.png)
Short Form : B<sub>s</sub>
#
ADVANTAGES:
- It has a time complexity of O(log n), which means it's faster than linear search
- Binary search is straightforward to implement and understand, requiring only basic programming constructs.
#
DISADVANTAGES:
1. Binary search can take a long time to sort small unsorted lists before searching for the desired value.

#
TASK
- [x] #Advanced Searching
- [x] Fastest
- [ ] Unsorted Array

> [!NOTE]  
> Please note this is the most fastest searching algorithm.

> [!TIP]
> If Anything is listed false please notify.

> [!IMPORTANT]
> Ensure that the data set is not small while searching.

> [!WARNING]
> Large Data Set might require less time complexity.

> [!CAUTION]
> Memory Risk.
 
#
Recurrence Relation : $`T(n) = 2T(\frac{n}{2}) +  k `$
Algorithm:
```
#include <iostream>
using namespace std;
int binarySearch(int array[], int x, int low, int high)
{
    // Repeat until the pointers low and high meet each
    // other
    while (low <= high) {
        int mid = low + (high - low) / 2;
 
        if (array[mid] == x)
            return mid;
 
        if (array[mid] < x)
            low = mid + 1;
 
        else
            high = mid - 1;
    }
    return -1;
}
```
## DIFFERENCES

 |Linear Search | Binary Search |
| :---------------- | :------: |
| In linear search input data need not to be in sorted.       |   In binary search input data need to be in sorted order.  |
| It is also called sequential search.           |   It is also called half-interval search.   |
| Multidimensional array can be used.    |  Only single dimensional array is used.  |

A footnote can also have multiple lines[^2].

[^1]: https://www.geeksforgeeks.org/linear-search-vs-binary-search/.
[^2]: https://www.programiz.com/dsa/binary-search
