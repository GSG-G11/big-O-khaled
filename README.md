BigPart 1

Simplify the following big O expressions as much as possible:

O(n + 10) => O (n)

O(100 * n) => O (n)

O(25) => O (1)

O(n^2 + n^3) => O (n^3)

O(n + n + n + n) => O (4n) = O (n)

O(1000 * log(n) + n) => O (n)

O(1000 * n * log(n) + n) => O (n * log(n))

O(2^n + n^2) => O (n^2)

O(5 + 3 + 1) => O (1)

O(n + n^(1/2) + n^2 + n * log(n)^10) => O (n^2)

Part 2

Determine the time and space complexities for each of the following functions. If you're not sure what these functions do, copy and paste them into the console and experiment with different inputs!


// 1.


//Time => O(n)

//Space =>O(1)

function logUpTo(n) {

  for (let i = 1; i <= n; i++) {
  
    console.log(i);
    
  }
  
}


// 2.

//Time => O(1)

//Space =>O(1)

function logAtMost10(n) {

  for (let i = 1; i <= Math.min(n, 10); i++) {
  
    console.log(i);
    
  }
  
}


// 3.

//Time => O(n)

//Space =>O(n)

function logAtLeast10(n) {

  for (let i = 1; i <= Math.max(n, 10); i++) {
  
    console.log(i);
    
  }
  
}


// 4.

//Time => O(n)

//Space =>O(n)

function onlyElementsAtEvenIndex(array) {

  let newArray = Array(Math.ceil(array.length / 2));
  
  for (let i = 0; i < array.length; i++) {
  
    if (i % 2 === 0) {
    
      newArray[i / 2] = array[i];
      
    }
    
  }
  
  return newArray;
  
}


// 5.

//Time => O(n^2)

//Space =>O(n)

function subtotals(array) {

  let subtotalArray = Array(array.length);
  
  for (let i = 0; i < array.length; i++) {
  
    let subtotal = 0;
    
    for (let j = 0; j <= i; j++) {
    
      subtotal += array[j];
      
    }
    
    subtotalArray[i] = subtotal;
    
  }
  
  return subtotalArray;
  
}
