# [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)

```
class Solution {
    public int[] productExceptSelf(int[] nums) {
        int n=nums.length;
        int pre[]=new int[n];
        int suf[]=new int[n];
        pre[0]=1;
        suf[n-2]=1;
        int ans[]=new int[n];
        for(int i=1;i<n;i++)
        {
            pre[i]=pre[i-1]*nums[i-1];
        }
        for(int j=n-2;j>=0;j--)
        {
            suf[j]=suf[j+1]*nums[j+1];
        }
        for(int i=0;i<n;i++)
        {
            ans[i]=pre[i]*suf[i];
        }
        return ans;
    }
}
```
>  - Present element = product of previous elements * product of next elements in the array
>
