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
<details><summary><b>Q. Iterate with Javascript While Loops<b></summary>
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
  
  <details><b>A. Iterate with Javascript While Loops<b></summary>
  ``` javacsript
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
