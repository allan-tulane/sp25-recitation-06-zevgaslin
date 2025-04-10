# CMPS 2200 Recitation 06
## Answers

**Name:**Zev Gaslin
**Name:**Joshua Haddad


Place all written answers from `recitation-07.md` here for easier grading.



- **2)**
- W(n) = 2 * W(n-1) + 1
- Root Dominated
- W(n) = O(2^n)

- **3)**
S(n) = S(n-1) +1
Leaf Dominated
S(n) = O(n)

- **4)**
The number of times each element of counts is called follows a pattern matching the Fibonacci sequence itself. This is because each Fibonacci call eventually gets down to using one of the first 2 calls, so the further along you go in the series, the more times you rely on the earlier calls rather than the later ones.

This shows that this method is not efficient because instead of just using the 2 numbers before it, each call is going all the way back to the beginning numbers in the sequence, resulting in repeated calculations of the same values.



- **6)**
- Each value is memoized after its called so the output is saved, so any one number only needs to be called once, and all other times after that its just looked up in the saved table. 

Work: Each number is computed exactly once, and each computation takes constant time (just an addition). Since we compute n numbers, the total work is O(n).

Span: Because of memoization, computing each number depends on all previous numbers sequentially. So even though work is reduced, the span is still O(n) due to this dependency chain.


- **8)**
- The maximum number of times that Fi will be read for any fibonachi value i is twice. This is becuase it will be saved to the list then called on to calculate the number in the list ahead of it then the number in the list two ahead of it. This is the maximum number of times it must be called. Based on this the work of this function is W(n) = O(n) because the for loop goes up to the number n and only refers to values in the for loop twice which adds no additional work. Similarly the span of this function is S(n) = O(n) beacuse each iteration of the loop is not parrallized.