# 26. Remove Duplicates from Sorted Array

[https://leetcode.com/problems/remove-duplicates-from-sorted-array/](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
This problem essentially boils down to returning the number of unique elements in the array. 
### Approach 1 :  Brute Force
The simplest approach would be to remove any element from the array which has previously occurred. 
Suppose, we are at an index ***i***, we traverse from 0 to i-1 and remove the elements which are the same as the element at ***i***. 
A careful observation along with the fact that the array is sorted, we only have to remove the i-1 element if it's the same. 
The only problem here is that removing an element from the middle of the array is an O(n) operation for each possible duplicate element. 

### Approach 2 :  Using a Map
Another approach would be to increment the count of all items encountered in a map and return  items whose count is 1. 
This approach suffers from bad space complexity, even though the time complexity is O(n).

 ### Approach 3:  Two Pointers at same end
A better approach would be to start with 2 pointers at the same end, let's say ***a*** and ***b***. 
We keep moving ***b*** forward until it's not equal to ***a***. We copy the value of the new ***b*** value to ***a+1***. 
Since we just have to return the number of unique elements, we only need to return 
This approach even works for cases where the array is not sorted but similar elements occur in groups like: [2, 2, 3, 1, 1, 1]

---
### Spin-Off 1: 
What if you were asked to design an algorithm to remove duplicates if the array was not sorted [in O(n) time] ?

### Spin-Off 2:
 Write a function which deletes all occurences of a given number from an array and the remaining elements have been shifted to the right and the deleted number has been replaced by 0's. Make sure that the ordering of the remaining elements has not been altered.
