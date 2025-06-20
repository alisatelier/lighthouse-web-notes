# Functions as Objects



Take the following code.
It is demonstrating values as functions and callbacks.

```javascript
let hitSongs = ["Cheap Thrills", "Shape of You", "Blinding Lights", "Levitating"];

const findFavourite = (songs, favourite) => {
  songs.forEach((song, index) => {
    if (song === "Cheap Thrills") {
      favourite(index);
    }
  });
};

const favouriteSong = (index) => {
  console.log("Favourite song is: " + hitSongs[index]);
};

findFavourite(hitSongs, favouriteSong);
```
## Functions as Values

In this section, we are declaring a function as a value. 'favouriteSong' is now a value containing the function.

```javascript
const favouriteSong = (index) => {
  console.log("Favourite song is: " + hitSongs[index]);
};
```

## Callback Function
In this section, 'findFavourite' is a reciever function with the parameter 'favourite' being a callback function, which can call any function as a value, but in this case we are using 'favouriteSong' as above.
We pass the  behaviour of 'favouriteSong' into the 'findFavourite' function by calling 'favourite()'.

```javascript
const findFavourite = (songs, favourite) => {
  songs.forEach((song, index) => {
    if (song === "Cheap Thrills") {
      favourite(index);
    }
  });
};
```
When we call the original function, we call our variable array of 'hitSongs' as well as our callback function 'favouriteSong'. We can do this with a value because the function has been set to one.

```javascript
findFavourite(hitSongs, favouriteSong);
```