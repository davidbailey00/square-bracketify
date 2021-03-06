# square-bracketify

Aren't regular curved brackets boring? Wouldn't it be fun to spice up your JavaScript?

Introducing Square-Bracketify, the latest in innovative, lightweight JavaScript libraries.

Go from this:

```js
console.log("Wow, a regular function call.", "How boring.");
```

To this:

```js
consoleLog[["This is much more exciting!", "I love square brackets!"]];
```

## Usage

Call `squareBracketify` to transform your boring functions into fun Square Bracket Functions™

```js
import squareBracketify from "square-bracketify";

function sayHello(firstName, lastName, times = 1) {
  for (let i = 0; i < times; i += 1) {
    console.log(`Hello, ${firstName} ${lastName}!`);
  }
}

// the squareBracketify function comes pre-squared
const sayHelloButWithSquareBrackets = squareBracketify[[sayHello]];

sayHelloButWithSquareBrackets[["David", "Bailey", 2]];
```

Look in `demo/script.js` for more usage examples.

## How does it work?

It (ab)uses the recent Proxy API to treat property access as a function call, along with hijacking `Array.prototype.toString` (which gets called whenever using accessing an property using a non-primitive key) in order to handle function arguments.

## Why did you make this?

I honestly don't know
