## Intro

Big O Notation is a way to formalize fuzzy counting.
It allows us to talk formally about how the runtime of an algorithm grows as the inputs grow.
It is used to analyze the performance of an algorithm.

A good perfroming algorithm is:

- faster
- occupies less memory during its operation
- is readable

In Big O we majorly concentrate on:

- Time Complexity
- Space Complexity

## Time Complexity

This is the number of operations the computer has to perform during the execution of an algorithm. This remains constant no matter what computer we are on.

```
function addUpTo(n){
    return n * (n + 1) / 2;
}
```

The above function has 3 operations: *, +, and / whether the input is 1 or 1000000.

```
function addUpTo(n) {
    let total = 0;
    for(let i = 1; i <= n; i++){
        total +=1;
    }
    return total;
}
```

This second function on the other hand has these operations from the first to the last if you consider n to be 3:
=(total = 0), =(let i = 1), <=n(i <= n) three times, +(i++) three times, +=(total +=1) three times.
Now consider an inpout like n = 1000, those will be 1000 times more operations in the for loop.

Given the examples above, the way Big O Notation is represented for the scenarios is as follows:

- constant operations: O(1) - no. of operations remains the same despite the input value
- inconsistent no. of operations: O(n) - no. of operations increases as the input value increases
- for a for loop inside another for loop: O(n * n)

## Space Complexity
The space that an algorithm takes up as the size of the input increases