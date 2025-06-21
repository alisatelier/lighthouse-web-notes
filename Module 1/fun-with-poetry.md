## Calling The Poets
```javascript
const verse0 = ["rustles", "of", "comfort", "reflected", "heat"]
const verse1 = ["sweeping", "entrance", "swiftly", "the", "feet"]
const verse2 = ["i", "wait", "for", "the", "drum", "the", "voice", "and", "the", "hum"]
const verse3 = ["lull", "me", "in", "waking", "sleep"]

const poem = [verse0, verse1, verse2, verse3]

//loops through array values and pushes the callback into a new array.
const map = function(array, callback) {
  const results = [];
  for (let item of array) {
    results.push(callback(item));
  }
  return results;
};
//this is the callback which finds first letter of the array value.
const firstLetter = (word) => word[0]

// placeholder for for lop[]
const verse = {};

//loops through the verses held in the array, 'poem' and applies the map function directly to the result, for each index of the poem.
for (let i = 0; i < poem.length; i++) {
  const poetry = poem[i];
  verse[i] = map(poetry, firstLetter);
}
// able to call the verse easily.
console.log(verse[0])
```

We were given the assignment to make the map function, and I wanted to use my knowledge to loop over the verses and apply the map function for each, instead of needing to call them with separate arguments.