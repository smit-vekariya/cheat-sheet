## 1. what is difference between var, let and const in javascript.
`Scope:`
- var: Function-scoped. A variable declared with var is accessible within the entire function it's declared in, or globally if declared outside any function.
- let: Block-scoped. A variable declared with let is only accessible within the block (defined by curly braces {}) it's declared in. 
- const: Block-scoped, similar to let.
```javascript
function example() {
  if (true) {
    var x = 10; // Function-scoped
    let y = 20; // Block-scoped
    const z = 30; // Block-scoped
  }
  console.log(x); // 10 (accessible within the function)
  // console.log(y); // Error: y is not defined (outside the block)
  // console.log(z); // Error: z is not defined (outside the block)
}
```
`Mutability:`
- var: Can be reassigned and redeclared within the same scope.
- let: Can be reassigned, but not redeclared within the same scope.
- const: Cannot be reassigned or redeclared. It must be initialized when declared.
```javascript
function example() {
  var x = 10; // Function scope, hoisted
  let y = 20; // Block scope, hoisted but in temporal dead zone
  const z = 30; // Block scope, hoisted, must be initialized

  // Using variables before declaration
  console.log(x); // Output: 10
  // console.log(y); // Error: ReferenceError: y is not defined
  // console.log(z); // Error: ReferenceError: z is not defined

  // Redeclaring variables
  var x = 5; // Allowed with var
  // let y = 40; // Error: Identifier 'y' has already been declared
  // const z = 40; // Error: Identifier 'z' has already been declared

  // Reassigning variables
  x = 3; // Allowed with var and let
  // z = 40; // Error: Cannot assign to constant variable 'z'
}
```
`Best Practices:`
- Use const for variables that shouldn't be reassigned (e.g., constants, configuration settings).
- Use let for most other variables.
- Avoid var in modern JavaScript development.