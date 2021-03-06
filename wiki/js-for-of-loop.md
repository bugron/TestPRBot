The `for..of` statement creates a loop iterating over iterable objects (including Array, Map, Set, Arguments object and so on), invoking a custom iteration hook with statements to be executed for the value of each distinct property.

```js
for (variable of object) {
  statement
}
```

|          | Description                          |
|----------|-------------------------------------|
| variable | On each iteration a value of a different property is assigned to variable.                                 |
| object | Object whose enumerable properties are iterated. |

[MDN link](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Statements/for...of) | [MSDN link](https://msdn.microsoft.com/library/dn858238%28v=vs.94%29.aspx?f=255&MSPPError=-2147217396) | [arguments\[@@iterator\]()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments/@@iterator)

## Examples
### Array
```js
let arr = [ "fred", "tom", "bob" ];

for (let i of arr) {
    console.log(i);
}

// Output:
// fred
// tom
// bob
```
### Map
```js
var m = new Map();
m.set(1, "black");
m.set(2, "red");

for (var n of m) {
console.log(n);
}

// Output:
// 1,black
// 2,red
```
### Set
```js
var s = new Set();
s.add(1);
s.add("red");

for (var n of s) {
console.log(n);
}

// Output:
// 1
// red
```
### Arguments object
```js
// your browser must support for..of loop
// and let-scoped variables in for loops

function DisplayArgumentsObject()
{
	for (let n of arguments) {
	console.log(n);
	}
}

DisplayArgumentsObject(1,"red");

// Output:
// 1
// red
```
