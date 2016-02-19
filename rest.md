```js
// *********** CLONE ARRAYS **************
const arr = [1, 2, 3];

// ES5
let cloned = arr.slice();
// ES6
let cloned = [...arr];


// ********** A BETTER ARGUMENTS *************
// ES5
function es5() {
	var args = Array.prototype.slice.call(arguments); // transform from *array-like* to array
}
function rest(a, b) {
	var restArgs = Array.prototype.slice.call(arguments, rest.length);
}

// ES6
function es6(...args) {}
function rest(a, b, ...rest) {}

// ************* A BETTER APPLY ***************
const args = ["hello", "world"];
// ES5
console.log.apply(console, args);

// ES6
console.log(...args);

// ************** IMMUTABLE REMOVE INDEX ***********
const arr = [1, 2, 3];
const removeIndex = 1;

// ES5
let clonedWithoutIndex = arr.slice(0, removeIndex).concat(arr.slice(removeIndex + 1));

// ES6
let clonedWithoutIndex = [
	...arr.slice(0, removeIndex),
	...arr.slice(removeIndex + 1)
];
```
