<details><summary><b>Q. Accessing Nested Arrays</b></summary>
As we have seen in earlier examples, objects can contain both nested objects and nested arrays. Similar to accessing nested objects, array bracket notation can be chained to access nested arrays.

Here is an example of how to access a nested array:
``` javascript
const ourPets = [
  {
    animalType: "cat",
    names: [
      "Meowzer",
      "Fluffy",
      "Kit-Cat"
    ]
  },
  {
    animalType: "dog",
    names: [
      "Spot",
      "Bowser",
      "Frankie"
    ]
  }
];

ourPets[0].names[1];
ourPets[1].names[0];
ourPets[0].names[1] would be the string Fluffy, and ourPets[1].names[0] would be the string Spot.
```
  ----
Using dot and bracket notation, set the variable secondTree to the second item in the trees list from the myPlants object.
  </details>
<details><summary>A. Accessing Nested Arrays</summary>
  
``` javascript
const myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }
];

const secondTree = myPlants[1].list[1];
```
</details>
<details><summary><b>Q. Record Collection</b></summary>
You are given an object literal representing a part of your musical album collection. Each album has a unique id number as its key and several other properties. Not all albums have complete information.

You start with an updateRecords function that takes an object literal, records, containing the musical album collection, an id, a prop (like artist or tracks), and a value. Complete the function using the rules below to modify the object passed to the function.

Your function must always return the entire record collection object.
If prop isn't tracks and value isn't an empty string, update or set that album's prop to value.
If prop is tracks but the album doesn't have a tracks property, create an empty array and add value to it.
If prop is tracks and value isn't an empty string, add value to the end of the album's existing tracks array.
If value is an empty string, delete the given prop property from the album.
Note: A copy of the recordCollection object is used for the tests.
</details>
<details><summary>A. Record Collection</summary>
 
```javascript
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  if (prop != 'tracks' && value) {
    records[id][prop] = value;
  }
  else if (prop == 'tracks' && !records[id].hasOwnProperty('tracks')) {
    records[id][prop] = [value];
  }
  else if (prop == 'tracks' && value) {
    records[id][prop].push(value);
  }
  else if (!value) {
    delete records[id][prop];
  }
  
  
  return records;
}

updateRecords(recordCollection, 5439, 'artist', 'ABBA');
```
  </details>
<details><summary><b>Q. Iterate with Javascript While Loops</b></summary>
You can run the same code multiple times by using a loop.

The first type of loop we will learn is called a while loop because it runs while a specified condition is true and stops once that condition is no longer true.
``` javascript
const ourArray = [];
let i = 0;

while (i < 5) {
  ourArray.push(i);
  i++;
}
```
In the code example above, the while loop will execute 5 times and append the numbers 0 through 4 to ourArray.

Let's try getting a while loop to work by pushing values to an array.

Add the numbers 5 through 0 (inclusive) in descending order to myArray using a while loop.
  </details>
  
  <details><summary>A. Iterate with Javascript While Loops</summary>
  
``` javascript
  // Setup
const myArray = [];

let i = 5;

while (i>-1) {
  myArray.push(i);
  i--;
}
// Only change code below this line
```
  </details>
  
  <details><summary><b>Q. Iterate with JavaScript For Loops</b></summary>
  You can run the same code multiple times by using a loop.

The most common type of JavaScript loop is called a for loop because it runs for a specific number of times.

For loops are declared with three optional expressions separated by semicolons:

for (a; b; c), where a is the initialization statement, b is the condition statement, and c is the final expression.

The initialization statement is executed one time only before the loop starts. It is typically used to define and setup your loop variable.

The condition statement is evaluated at the beginning of every loop iteration and will continue as long as it evaluates to true. When the condition is false at the start of the iteration, the loop will stop executing. This means if the condition starts as false, your loop will never execute.

The final expression is executed at the end of each loop iteration, prior to the next condition check and is usually used to increment or decrement your loop counter.

In the following example we initialize with i = 0 and iterate while our condition i < 5 is true. We'll increment i by 1 in each loop iteration with i++ as our final expression.
``` javascript
const ourArray = [];

for (let i = 0; i < 5; i++) {
  ourArray.push(i);
}
```
ourArray will now have the value [0, 1, 2, 3, 4].

Use a for loop to push the values 1 through 5 onto myArray.
  
  </details>
  <details><summary>A. Iterate with JavaScript For Loops</summary>
  
 ``` javascript
  // Setup
const myArray = [];

// Only change code below this line

for (let i = 1; i < 6; i++) {
  myArray.push(i);
}
```
  </details>
  <details><summary><b>Q. Iterate Odd Numbers With a For Loop</b></summary>
    For loops don't have to iterate one at a time. By changing our final-expression, we can count by even numbers.

We'll start at i = 0 and loop while i < 10. We'll increment i by 2 each loop with i += 2.

  ``` javascript
const ourArray = [];

for (let i = 0; i < 10; i += 2) {
  ourArray.push(i);
}
  ```
ourArray will now contain [0, 2, 4, 6, 8]. Let's change our initialization so we can count by odd numbers.

Push the odd numbers from 1 through 9 to myArray using a for loop.
  </details>
    <details><summary>A. Iterate Of Numbers With a For Loop</summary>
      
``` javascript
// Setup
const myArray = [];

// Only change code below this line

for (let i = 1; i < 10; i++) {
  if (i%2 == 1) {
  myArray.push(i);
  }
}
```
</details>
      <details><summary><b>Q. Count Backwards With a For Loop</b></summary>
A for loop can also count backwards, so long as we can define the right conditions.

In order to decrement by two each iteration, we'll need to change our initialization, condition, and final expression.

We'll start at i = 10 and loop while i > 0. We'll decrement i by 2 each loop with i -= 2.

``` javascript
 const ourArray = [];

for (let i = 10; i > 0; i -= 2) {
  ourArray.push(i);
}
        
```
ourArray will now contain [10, 8, 6, 4, 2]. Let's change our initialization and final expression so we can count backwards by twos to create an array of descending odd numbers.

Push the odd numbers from 9 through 1 to myArray using a for loop.
      </details>
