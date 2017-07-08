## Arrays 

### `join()`

```
var beatles = ['john','paul','george','ringo']
beatles.join(' ') // "john paul george ringo"
```

### `pop()`

```
var beatles = ['john','paul','george','ringo']
var last = beatles.pop() // "ringo"
beatles // ["john", "paul", "george"]
```

### `sort()`

```
var beatles = ['john','paul','george','ringo']
var orderedBeatles = beatles.sort()
orderedBeatles // ["george", "john", "paul", "ringo"]

var numbers = [1,45,2,67,3,34,3,23]
numbers.sort()
// [1, 2, 23, 3, 3, 34, 45, 67]

numbers.sort( function(a, b) {
  return a - b;
})
// [1, 2, 3, 3, 23, 34, 45, 67]
```

### `slice()`

```
var fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango'];
var citrus = fruits.slice(1, 3);
citrus // 'Orange', 'Lemon'
```

### `splice()`

```
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
myFish.splice(2, 1); 
```

### `push()`

```
var fruits = [];
fruits.push('oranges')
fruits.push('apples')
```

### `shift()`

```
var fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango'];
fruits.shift() // "Banana"
fruits // ["Orange", "Lemon", "Apple", "Mango"]
```

### `includes()` 

```
var a = [1, 2, 3];
a.includes(2); // true 
a.includes(4); // false
```

### `unshift()`

```
var fruits = ['Banana', 'Orange', 'Lemon', 'Apple', 'Mango'];
fruits.unshift("Melon")
fruits // ["Melon", "Orange", "Lemon", "Apple", "Mango"]
```

## Arrays (higher order functions)

### `forEach`

```
var myArray = [2,5,13,9]

// OLD Way

for (var i=0; i<myArray.length; i++) {
  console.log(myArray[i]*2)
}

// MODERN Way

[2,5,13,9].forEach( function(itemNumber) { 
  console.log(itemNumber*2)
} )

// MODERN Way better

function showMultiplyBy2(item) { 
  console.log(item*2)
}

[2,5,13,9].forEach( showMultiplyBy2 )
```

### `map`

```
arr.map(callback[, thisArg])

var numbers = [1, 5, 10, 15];
var doubles = numbers.map(function(x) {
   return x * 2;
});
// doubles is now [2, 10, 20, 30]

var numbers = [1, 4, 9];
var roots = numbers.map(Math.sqrt);
// roots is now [1, 2, 3]

```

### `filter()`

```
arr.filter(callback[, thisArg])

var words = ["spray", "limit", "elite", "exuberant", "destruction", "present"];
var longWords = words.filter(function(word){
  return word.length > 6;
})

// return words longest than 6 letters
// Filtered array longWords is ["exuberant", "destruction", "present"]
```

### `reduce()`

```
arr.reduce(callback[, initialValue])

var total = [0, 1, 2, 3].reduce(function(sum, value) {
  return sum + value;
}, 0);
// total is 6

var flattened = [[0, 1], [2, 3], [4, 5]].reduce(function(a, b) {
  return a.concat(b);
}, []);
// flattened is [0, 1, 2, 3, 4, 5]

```
