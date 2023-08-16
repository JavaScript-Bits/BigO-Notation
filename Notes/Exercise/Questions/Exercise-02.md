**Use Big O Notation to describe the time complexity of the following function that sums up all the numbers from a given array:**

```js

const sumOfArray = (array) => {
  let sum = 0;

  for(let i = 0; i < array.length; i++){
    sum += array[i];
  }
  return sum;
}

```

The time complexity for  `sumOfArray` is: `O(n)`. The number of operations that will be used in the for loop will increase as the input increases.