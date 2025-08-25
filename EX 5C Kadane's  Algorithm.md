# EX 5C Kadane's Algorithm
## DATE:
## AIM:

To write a python program to find the maximum contiguous subarray.

## Algorithm

1. Read integer `n` (number of elements in array).
2. Read `n` integers into array `a`.
3. Initialize:

   * `max_till_now = a[0]` (stores the overall maximum sum found so far)
   * `max_ending = 0` (stores the sum of the current subarray)
4. Loop through each element in the array:

   * Add the current element to `max_ending`
   * If `max_ending < 0`, reset it to 0
   * If `max_till_now < max_ending`, update `max_till_now`
5. Return `max_till_now` as the maximum subarray sum.

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.


Developed by: SINGARAVETRIVEL S
Register Number: 212222220048
*/
```
```python
def maxSubArraySum(a,size):
    
    max_till_now = a[0]
    max_ending = 0
    
    for i in range(0, size):
        max_ending = max_ending + a[i]
        if max_ending < 0:
            max_ending = 0
        
        
        elif (max_till_now < max_ending):
            max_till_now = max_ending
            
    return max_till_now
    
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
  
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```

## Output:

![image](https://github.com/user-attachments/assets/0349239c-ae84-4002-b782-aa49e0c7bb61)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
