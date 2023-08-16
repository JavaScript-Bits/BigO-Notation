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
The space that an algorithm takes up as the size of the input increases.

When we talk about space complexity we mostly refer to `Auxiliary Space Complexity` which refers to the space required by the algorithm, not including space taken up by the inputs.

#### Rules of Thumb
- Most primitives(booleans, numbers, undefined, null) are constant space.
- Strings require O(n) space (where n is the string length)
- Reference types are generally O(n), where n is the length (for arrays) or the number of keys (for objects)

Example 1:
```
function addUpTo(n) {
    let total = 0;
    for(let i = 1; i <= n; i++){
        total +=1;
    }
    return total;
}
```

Here we have two variables taking up space while the algorithm executes: `total` and `i`. Regardless of the size of the input there will always be two spaces used hence the function above represents `O(1)` space complexity.

Example 2:

```
function double(arr) {
    let newArr = [];
    for(let i = 0; i < arr.length; i++){
        newArr.push(2 * arr[i])
    }
    return newArr;
}
```
This function on the other hand is `O(n)` since the array length grows hence more space occupied depending on the items in the input array.