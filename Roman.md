# 13 [Roman to Integer](https://leetcode.com/problems/roman-to-integer/)

```
class Solution {
    public int romanToInt(String s) {
        char a[]=s.toCharArray();
        HashMap<Character,Integer>mp=new HashMap<>();
        mp.put('I',1);
        mp.put('V',5);
        mp.put('X',10);
        mp.put('L',50);
        mp.put('C',100);
        mp.put('D',500);
        mp.put('M',1000);
        int v=0;
        int sum =0;
        for(int i=a.length-1;i>=0;i--)
        {
            if(mp.get(a[i])>=v){
                sum=sum +mp.get(a[i]);
                v=mp.get(a[i]);
            }
            else{
                sum =sum-mp.get(a[i]);
            }  
        }
        return sum;
    }
}
```
