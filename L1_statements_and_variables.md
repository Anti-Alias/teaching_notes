# HTML
## Minimal HTML template that inlines its JavaScript

index.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Sexy Singles in Your Area!!!</title>
    </head>
    <body>
        <p>Hello, world</p>
        <!-- Embedded JavaScript, don't do this -->
        <script>
            window.alert('Hello, world!');
            window.alert('I can only access HTML above me, but not below me!');
            window.alert('You should probably put me in another file...');
        </script>
    </body>
</html>
```

## Minimal HTML template that links to other JavaScript with a URL

index.html
```html
<!DOCTYPE html>
<html>
    <head>
        <title>Sexy Singles in Your Area!!!</title>
    </head>
    <body>
        <p>Hello, world</p>
        <script src="script.js"></script>
    </body>
</html>
```

# JavaScript

## Statements
Statements are separated by a ; character, or newlines.
JavaScript runs each statement one at a time from top to bottom.

Statements separated by newlines only.
```javascript
console.log('statement 1')
let x = 'statement 2'
window.alert('statement 3')
```

Statements separated by semicolons AND newlines. This is encouraged by most; don't ask why.
```javascript
console.log('statement 1');
let x = 'statement 2';
window.alert('statement 3');
```

One-liner. Works the same as above.
Semicolons allow multiple statements on one line, though this is SUPER uncommon.
Hard to read.
```javascript
console.log('statement 1'); let x = 'statement 2'; window.alert('statement 3');
```


## Logging
```javascript
window.alert('Ur mom!');    // Annoying popup window. Never use on a real site. JS will halt until "OK" is pressed. Everything fucking freezes on the page.
alert('Ur mom!');           // window is optional. Functionally equivalent.
console.log('Ur mom!');     // Logs a message in the console. Does not stop the page. Great for figuring out bugs. User does not see this output
```

You can view the output of ```console.log()``` by hitting F12 in chrome and navigating to "Console".

## Variables
```javascript
let num = 3;                // Create a new variable called 'num' and set it to 3. It has a "datatype" of "Number".
num = 2;                    // Re-assigns an existing variable.
const message = 'ur mom';   // Create a new variable called 'message' and set it to 'ur mom' . It has a "datatype" of "String". CANNOT BE REASSIGNED. If you try, the code stop and outputs an error in the console. 
```

## Let VS Const
Both `let` and `const` are keywords for declaring new variables that don't yet exist.
`let` will let you reassign the variable, while `const` (constant) will not.
Attempting to reassign a `const` variable will cause the program to throw an error (crash, most of the time).

Most variables don't change once created, so `const` will typically be your go-to.
It signals to other programmers that your varible doesn't change once created, letting them make quick assumptions without digging too deep through the code.
It's a good idea to use `let` ONLY when you need to reassign a variable.
We'll get into when that's necessary later.

## Redeclaring is Invalid
```javascript
let x = 1;
let x = 2;      // JS will error when it hits this line. x already exists.
```

```javascript
const y = 1;
const y = 2;    // JS will error when it hits this line. y already exists.
```

```javascript
let z = 1;
const z = 2;    // JS will error when it hits this line. z already exists.
```