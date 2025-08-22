# Data Types
All values have a "data type".
We've seen ```String``` and ```Number``` so far.
Here's a list of the main JavaScript types:


## String
Stores text.
```javascript
let a = '123';
let b = "abc";  // Double quotes also work. No difference. Single is preferred by most.
let c = a + b;  // + symbol will "concatenate" these to "123abc". So, it will stitch them together. 
```

## Number
Stores numeric value that you can do arithmetic with.
```javascript
let a = 0.5;
let b = 0.6; 
let c = a + b;  // Value is 1.1
```
## Boolean
Stores either true or false.
Useful when doing "conditional logic"
```javascript
let isProgramming = true;   // Stores boolean value of true
let isGardening = false;    // Stores boolean value of false 
let isAmazing = 10 > 9;     // Stores boolean value of true

if(isProgramming) {
    console.log('This line of code runs!');
    console.log('So does this one!');
}

if(isGardening) {
    console.log('This line of code does NOT run!');
    console.log('Nor does this one...');
    let message = 'Noooor this one!';
    console.log(message);
}

if(isAmazing) {
    console.log('This line of code runs!');
}

if(11 > 9) {
    console.log('This line of code runs!');
}

let a = 10;
if(7 > a) {
    console.log('This line of code does NOT!');
}

if(true) {
    console.log('This line of code runs!');
}

if(false) {
    console.log('This line of code does NOT run!');
}
```

## Array
Stores a list of values of any type.
```javascript
let shopping_list_a = ['apples', 'steak', 'corn'];      // List of 3 strings
let numbers = [1, 2, 3];                                // List of 3 numbers 
let eggs = 'eggs';                                      // Regular string, used below...
let shopping_list_b = ['milk', eggs, 3, [4], false];    // List of 4 values of various types 
let empty_list = [];                                    // Empty list, duh... 
```

## Object
Acts as a bag of named values.
```javascript
let dog = { name: 'Fido', age: 3, isGoodBoy: true };    // One-liner object.
let cat = {                                             // Multi-liner, easier to read.
    species: 'cat',
    name: 'Garfield',
    lives: 9,
    hasWings: false,
    owner: {
        name: 'John',
        species: 'Human',
    },
}; // Optional, but don't forget the good-boi semicolon. 

console.log(dog.name);          // Outputs "Fido" to console.
console.log(cat.lives);         // Outputs 9 to console.
console.log(cat.owner.species); // Outputs "Human" to console.
```
Note: ```console``` and ```window``` are both built-in objects in JavaScript.
You've already been using them!

## Function
A snippet of code that you can run, or "call" or "invoke" whenever you want.
Basically, you're making your own "command" out of existing commands.
Great for code reuse, vaguely similar to an HTML template with parameters that you can reuse.
```javascript
let doMath = function(a, b) {       // Declare function with two input variables.
    let c = a * b + 1;              // c is a variable local to function. Goes away when finished.
    return c;                       // Output of function. 
}                                   // End of function declaration

let two = doMath(1, 1);             // Passes in 2 numbers, outputs a number, stores in variable.
let seven = doMath(2, 3);           // Passes in 2 numbers, outputs a number, stores in variable. 
console.log(two);                   // Ouputs 2
console.log(seven);                 // Ouputs 7 
console.log(doMath(3, 3));          // Ouputs 10
console.log(c);                     // FAILS! c was local to the body of the "doMath" function.
```

Note, this is a more typical function delcaration.
It's equivalent to the above function declaration in most ways, but there are some subtle differences that aren't worth getting into here.

```javascript
function doMath(a, b) {
    let c = a * b + 1;
    return c;
}
```