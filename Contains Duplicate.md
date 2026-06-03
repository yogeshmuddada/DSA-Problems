
# [217. Contains Duplicate](https://leetcode.com/problems/contains-duplicate/)

### HashMap:
```
class Solution {
    public boolean containsDuplicate(int[] nums) {

        HashMap<Integer, Integer> mp=new HashMap<>();
        for(int i=0;i<nums.length;i++){
            if(mp.containsKey(nums[i]))
            return true;
            else
            mp.put(nums[i],i);
        }
        return false; 
    }
}
```
> - if we stored the values in ***hashmap*** then we can above to retrive it fastly and we don't need inner forloop also.
> - if we used ***hashset*** then also we can reduced the time complexity and space complexit.

### Hashset
```
class Solution {
    public boolean containsDuplicate(int[] nums) {

        HashSet<Integer> hs=new HashMap<>();
        for(int i=0;i<nums.length;i++){
            if(!hs.add(nums[i])
            return true;
        }
        return false; 
    }
}
```
