# EX 5B Coin Change Problem
## DATE: 
## AIM:
To compute the fewest number of coins that we need to make up the amount given.


## Algorithm
1. Read integer n (number of coin denominations).

2. Read integer amt (target amount).

3. Read n coin values into a list s.

4. Initialize a DP array dp of size amt + 1 with all values as infinity.

5. Set dp[0] = 0 (base case: 0 coins to make amount 0).

6. For each coin in s:
   1. For each amount i from coin to amt:
      1. Update dp[i] = min(dp[i], dp[i - coin] + 1)

7. If dp[amt] is not infinity, return dp[amt] (minimum coins needed); else return -1.

## Program:
```
/*
Create a python function to compute the fewest number of coins that we need to make up the amount given.

.
Developed by: SINGARAVETRIVEL S
Register Number: 212222220048
*/
```
```python
class Solution(object):
   def coinChange(self, coins, amount):
       dp = [float('inf')] * (amount + 1)
       dp[0]=0
       for coin in coins:
           for i in range(coin, amount + 1):
               dp[i] = min(dp[i], dp[i - coin] + 1)
       return dp[amount] if dp[amount]!=float('inf') else -1
      
ob1 = Solution()
n=int(input())
s=[]
amt=int(input())
for i in range(n):
    s.append(int(input()))


print(ob1.coinChange(s,amt))
```

## Output:

![image](https://github.com/user-attachments/assets/554d3909-c4e6-4be8-876d-8cf60418d1f0)


## Result:
Thus the program was executed successfully for finding the minimum number of coins required to make amount.
