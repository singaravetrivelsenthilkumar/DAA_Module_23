# EX 5D Minimum Jump to Reach End Array
## DATE: 
## AIM:
To write a python program for finding the minimum number of jumps needed to reach end of the array using Dynamic Programming.


## Algorithm

1. Read integer `n` (number of elements in the array).
2. Read `n` integers into array `arr`.
3. If `n == 0` or `arr[0] == 0`, return infinity (end cannot be reached).
4. Initialize a `jumps[]` array of size `n` with all values `∞` and set `jumps[0] = 0`.
5. For each position `i` from 1 to `n - 1`:

   * For each position `j` from 0 to `i - 1`:

     * If `i` is reachable from `j` (i.e., `i <= j + arr[j]`) and `jumps[j]` is not `∞`:

       * Update `jumps[i] = min(jumps[i], jumps[j] + 1)`
       * Break inner loop (first valid jump found)
6. Return `jumps[n-1]` as the minimum number of jumps to reach the end.

## Program:
```
/*
To implement the program to finding the minimum number of jumps needed to reach end of the array.

Developed by: SINGARAVETRIVEL S
Register Number: 212222220048
*/
```
```python
def minJumps(arr, n):
    jumps = [0 for i in range(n)]
 
    if (n == 0) or (arr[0] == 0):
        return float('inf')
 
    jumps[0] = 0
    for i in range(1, n):
        jumps[i] = float('inf')
        for j in range(i):
            if (i <= j + arr[j]) and (jumps[j] != float('inf')):
                jumps[i] = min(jumps[i], jumps[j] + 1)
                break
    return jumps[n-1]
arr = []
n = int(input()) #len(arr)
for i in range(n):
    arr.append(int(input()))
print('Minimum number of jumps to reach','end is', minJumps(arr,n))

```

## Output:

![image](https://github.com/user-attachments/assets/1b156320-6b5c-4f9c-9d2c-1a3a72efa7ca)


## Result:
Thus the program was executed successfully for finding the minimum number of jumps to reach end.
