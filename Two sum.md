
# Two Sum Solution

### Bruteforce method:

```
class Solution {
    public int[] twoSum(int[] nums, int target) {
       int n = nums.length;
       int res[] = new int[2];

       for (int i = 0; i < n; i++) {
           for (int j = i + 1; j < n; j++) {
               if (nums[j] == target - nums[i]) {
                   return new int[] {i, j};
               }
           }
       }

       return null;
    }
}
```

### Using HashMap:
```
class  Solution {
public  int[] twoSum(int[] nums, int  target) {
HashMap<Integer,Integer> mp=new  HashMap<>();
for(int  i=0;i<nums.length;i++){
			int  r=target-nums[i];
			if(mp.containsKey(r))
					return  new  int[]{mp.get(r),i};
			mp.put(nums[i],i);
					}
	return  new  int[]{};
		}
}
```
