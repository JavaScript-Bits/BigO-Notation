**Write a function that accepts an array of strings and return a new array that only contains the strings that start with the character 'd'. Use Big O Notation to describe the time complexity of the function.**

```js
const returnString = (arr) => {
        return arr.filter(string => string.toLowerCase().startsWith('d'));
}
```
The above function will have a time complexity of `O(n)`. This is because the filteration operations will increase as the input increases.