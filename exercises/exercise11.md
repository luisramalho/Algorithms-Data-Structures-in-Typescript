## Exercise

Given two strings, write a method to decide if one is a permutation of the other.

## Solution

```js
var permuteStrings = function(str1, str2){
  if(str1.length !== str2.length) return false;

  let chars1 = str1.split('');
  let chars2 = str2.split('');

  return chars1.sort().join() === chars2.sort().join();
}


console.assert(permuteStrings('BALL', 'LALB') === true, 'Implementation is wrong1');
console.assert(permuteStrings('BALL', 'laab') === false, 'Implementation is wrong2');
console.assert(permuteStrings('BALL', 'LABBB') === false, 'Implementation is wrong3');
```