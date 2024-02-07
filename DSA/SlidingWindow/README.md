# Sliding Window:
`array/string`+`subarray/substring`+`sum/largest/smallest`+`k(window size)` = Sliding Window Problem

## Brute force:
- In the naive solution we use a O(N^2) solution
```cpp
for(int i -> 0){
    // where k is the size of subarray specified
    for(int j = i -> i + k){
        condition;
    }
}
```

- To improve on this we use sliding window. We need 2 conditions to implement SW:
    - If **repetitive work** is taking place
    > In the above example we will find 1+2+3 then 2+3+4 so we repeatedly find the sum of 2+3 and so on.
    - If a operation is needed to be performed on that sub-something

### Types of Sliding Window:
**Fixed Window**: Fixed operation like max or min
- We first take a start(i) and end(j) pointer where the window length is `j-i+1`
    - First we set the sliding window
        - `j-i+1 < k` -> `j++`
    - When the condition is met `j-i+1==k` we need to maintain this size by `j++` && `i++` and apply the condition.
    
**Variable Window**: When we need to find smallest or largest window size
