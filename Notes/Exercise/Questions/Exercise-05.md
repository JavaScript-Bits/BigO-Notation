**The following function calculates the median from an ordered array. Describe its time complexity in terms of Big O Notation:**

```js

const median (array) => {
  const middle = Math.floor(array.length / 2);

  if(array.length % 2 === 0) {
    return (array[middle - 1] + array[middle]) / 2;
  }
  return array[middle];
}

```