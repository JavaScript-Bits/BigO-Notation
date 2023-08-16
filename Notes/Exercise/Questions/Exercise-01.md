**Use Big O Notation to describe the time complexity of the following function that determines whether a given yaer is a leap year:**

```js

function isLeapYear(year){
  return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);
}

````

The time complexity for  `isLeapYear` is: `O(1)`. Regardless of the input the algorithm will still go through the same number of operations during operation.