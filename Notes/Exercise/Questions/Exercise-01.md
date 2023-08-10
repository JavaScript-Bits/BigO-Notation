**Use Big O Notation to describe the time complexity of the following function that determines whether a given yaer is a leap year:**

```js

function isLeapYear(year){
  return (year % 100 === 0) ? (year % 400 === 0) : (year % 4 === 0);
}

````