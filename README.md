# Check Duplicates in Array

## Problem
Given an array of integers `nums`, determine whether the array contains any duplicate elements.  
Return **true** if any value appears at least twice in the array, otherwise return **false**.

---

## Approach
1. First, sort the array using `Arrays.sort()`.
2. After sorting, duplicate elements will appear **next to each other**.
3. Traverse the array and compare each element with its previous element.
4. If `nums[i] == nums[i-1]`, a duplicate exists.

---

## Algorithm
1. Sort the array.
2. Loop from `i = 1` to `n-1`.
3. If `nums[i] == nums[i-1]` → return `true`.
4. If loop completes → return `false`.

---

## Java Implementation

```java
import java.util.Arrays;

class Solution {
    public boolean checkDuplicates(int nums[]) {
        Arrays.sort(nums);

        for(int i = 1; i < nums.length; i++){
            if(nums[i] == nums[i - 1]){
                return true;
            }
        }

        return false;
    }
}
Example

Input

nums = [6, 9, 5, 3, 2, 6, 6, 4]

Sorted Array

[2, 3, 4, 5, 6, 6, 6, 9]

Output

true
Time Complexity
O(n log n)

(Sorting takes the most time)

Space Complexity
O(1)
Author

Sanjeev Sharma.

