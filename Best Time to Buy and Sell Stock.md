# [121. Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)

```
class Solution {
    public int maxProfit(int[] prices) {

        int buy=Integer.MAX_VALUE;
        int profit=0;
        int tsp=0; //if sell today then profit
        for (int i=0;i<prices.length;i++)
        {
            if(prices[i]<buy)
            {
                buy=prices[i];
            }
            tsp=prices[i]-buy;
            if(profit<tsp)
                profit=tsp;
        }
        return profit;
    }
}
```
