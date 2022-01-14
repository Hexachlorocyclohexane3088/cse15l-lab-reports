#Given an *array* of *integers* nums and an *integer* target, return indices of the two numbers such that they add up to target.    
---
[Link](https://leetcode.com/problems/two-sum/)   
**Solution:**  
[Link](https://leetcode.com/problems/two-sum/discuss/3/Accepted-Java-O(n)-Solution)  
---
![Image](https://ucsdnews.ucsd.edu/news_uploads/Resized_Geisel_Library_08.31.jpg) 
##1. One
2. Two
3. Three
> Related topics
* Hash Table
* Two Pointer
* Sorting

`this is a O(n) time complexity solution `  

  

```
# the solution to the twoSum
import java.util.HashMap;

class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer,Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            if (map.containsKey(target - nums[i])) {
                int[] res = {i, map.get(target - nums[i])};
                return res;
            }
            map.put(nums[i], i);
        }
        return null;
        
    }
}
```
  
