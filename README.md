# Study-Notes
// Just note or thought throughout my study journey

// To check if the Javascrip object has a specific property called "top":
myObj.hasOwnProperty("top");

// When adding object to an array:
each object in the array should be seperated by cama ",".

// Array Manipulate methonds:
Add sth. to an array(at the end): arrayName.push();
Add sth. to an array(at the begining): arrayName.unshift();
delete sth. from arry(from the beginning): arrayName.shift();
delete sth. from array(from the ending), and return the deleted element: arrayName.pop();

// Recursion:
multiply the first n elements of an array to create the product of those elements. Using a for loop, you could do this:

  function multiply(arr, n) {
    var product = 1;
    for (var i = 0; i < n; i++) {
        product *= arr[i];
    }
    return product;
  }
However, notice that multiply(arr, n) == multiply(arr, n - 1) * arr[n - 1]. That means you can rewrite multiply in terms of itself and never need to use a loop.

  function multiply(arr, n) {
    if (n <= 0) {
      return 1;
    } else {
      return multiply(arr, n - 1) * arr[n - 1];
    }
  }
  
  The ES5 code below uses apply() to compute the maximum value in an array:

var arr = [6, 89, 3, 45];
var maximus = Math.max.apply(null, arr); // returns 89
We had to use Math.max.apply(null, arr) because Math.max(arr) returns NaN. Math.max() expects comma-separated arguments, but not an array. The spread operator makes this syntax much better to read and maintain.

const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr); // returns 89
...arr returns an unpacked array. In other words, it spreads the array. However, the spread operator only works in-place, like in an argument to a function or in an array literal. The following code will not work:

const spreaded = ...arr; // will throw a syntax error
  
// When using the destruction method to change the stuff in the object, write the origional prop. name first, then ":", then the new name.
