# Apuntes Array

- array lenght 

```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let size = fruits.length;
```

- array toString()

```js
document.getElementById("demo").innerHTML = fruits.toString();
```

- array at()

```js
let fruit = fruits[2]; // apple
```

- array join()

The join() method also joins all array elements into a string.
```js
fruits.join(" * ")
Banana * Orange * Apple * Mango
```

- array pop()

The pop() method removes the last element from an array:
```js
fruits.pop();
```

The pop() method returns the value that was "popped out":

```js
let fruit = fruits.pop();
```

- array push()

The push() method adds a new element to an array (at the end):

The push() method returns the new array length:


```js
let length = fruits.push("Kiwi"); // 5
```


- array shift()

The shift() method removes the first array element and "shifts" all other elements to a lower index.

The shift() method returns the value that was "shifted out":
```js
let fruit = fruits.shift(); 

/*
Banana

Orange,Apple,Mango
*/
```

- array unshift()

 The unshift() method adds a new element to an array (at the beginning), and "unshifts" older elements:

```js
 fruits.unshift("Lemon");

 The unshift() method returns the new array length:

 // Lemon,Banana,Orange,Apple,Mango

 ```

 ...

 Array elements are accessed using their index number:

```js

const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi";

```

- for change the array...

an easy way:

```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi";

```

- Delete array

Using delete() leaves undefined holes in the array.

delete fruits[0]; // The first fruit is: undefined


Use pop() or shift() instead.

- concatenate arrays

The concat() method creates a new array by merging (concatenating) existing arrays:

```js

const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];

const myChildren = myGirls.concat(myBoys);

```
Example (Merging an Array with Values)

```js
const arr1 = ["Emil", "Tobias", "Linus"];
const myChildren = arr1.concat("Peter");
```

- array flat()

The flat() method creates a new array with sub-array elements concatenated to a specified depth.

```js
const myArr = [[1,2],[3,4],[5,6]];
const newArr = myArr.flat(); // 1,2,3,4,5,6
```

- flatMap()

```js
const newArr = myArr.flatMap(x => [x, x * 10]);
// 1,10,2,20,3,30,4,40,5,50,6,60
```

- Array splice()

The first parameter (2) defines the position where new elements should be added (spliced in).

The second parameter (0) defines how many elements should be removed.

The rest of the parameters ("Lemon" , "Kiwi") define the new elements to be added.

```js

const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");

```

With clever parameter setting, you can use splice() to remove elements without leaving "holes" in the array:

```js
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);

```

The first parameter (0) defines the position where new elements should be added (spliced in).

The second parameter (1) defines how many elements should be removed.

The rest of the parameters are omitted. No new elements will be added.

...

The difference between the new `toSpliced()` method and the old `splice()` method is that the new method creates a new array, keeping the original array unchanged, while the old method altered the original array.


- array slice()

The slice() method slices out a piece of an array into a new array:

```js
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1); // Orange,Lemon,Apple,Mango

```
The slice() method creates a new array.

The slice() method does not remove any elements from the source array.
...

The slice() method can take two arguments like slice(1, 3).

The method then selects elements from the start argument, and up to (but not including) the end argument.

- array toString()

JavaScript automatically converts an array to a comma separated string when a primitive value is expected.