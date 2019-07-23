# 19-7-23
7. 整数反转

/**
2019.7.23
LeetCode
整数反转
**/

class Solution {
    public int reverse(int x){
      int ans=0;
      while(x!=0){
        int pop=x%10;
        if(ans>Integer.MAX_VALUES/10 || (ans=Integer.MAX_VALUES/10 && pop>7))
          return 0;
        if(ans<Integer.MIN_VALUES/10 || (ans=Integer.MIN_VALUES/10 && pop<-8))
          return 0;
        ans=ans*10+pop;
        x/=10;
      }
      return ans;
    }
}

/*
示例 1:
输入: 123
输出: 321
示例 2:
输入: -123
输出: -321
示例 3:
输入: 120
输出: 21
*/
