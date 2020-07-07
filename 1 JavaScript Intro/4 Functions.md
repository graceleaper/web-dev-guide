# Function

- A function is a reusable block of code. It's like a math equation: it receives inputs to produce outputs

## Parts of a function

* 'function' keyword
* name of function
* parens that hold parameters or arguments
* opening and curly braces

```
function aCoolFunc() {
    console.log('hello world')
}
```

- In Chrome console: 

```
// invoke a function
aCoolFunc()
```

- NOTE: the 'function' keyword is what 
distinguishes a function declaration from 
a function invokation

- We can run a function as many times as we want

## Parameters and arguments in a function

* You can have as many arguments as you want in a function

```
function myMessage(name) {
    console.log('hello ' + name + '!')
}

//can call a function with different parameter values
myMessage('Jack')
myMessage('Will')

let newUser = 'Velma'
myMessage(newUser)
```

```
function myMessage(firstName, lastName) {
    console.log('Hello, ' + firstName + ' ' + lastName)
}

/* the variables 'firstName' and 'lastName' don't
have to match the parameters from our 
myMessage function
*/

let bananas = 'John'
let oogabooga = 'Frett'
myMessage(bananas, oogabooga)
```

- We've been console.logging code in functions

## Return keyword
* The `return` keyword will return us a value where
the function was invoked

```
function addition (a, b) {
    let sum = a + b
    return sum
}

console.log(addition(7, 5))
```

* `return` is different from `console.log`
* `console.log` displays value in the console
* So in the above code block, addition(7,5) will return 12

```
let y = 5 + addition(7,5)
console.log(y) // returns 17
```

```
function isEven(x) {
    if(x % 2 === 0) {
        return true
    } else {
        return false
    }
}

console.log(isEven(555)) // return false
console.log(isEven(400)) // return true
```