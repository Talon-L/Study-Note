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
