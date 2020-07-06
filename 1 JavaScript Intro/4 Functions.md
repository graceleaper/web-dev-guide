* FUNCTION *

- a reusable block of code
- like math equations -- give inputs to produce outputs

PARTS OF A FUNCTION:
- 'function' keyword
- name of function
- parens that hold parameters or arguments
- opening and curly braces

function aCoolFunc() {
    console.log('hello world')
}

in Chrome console: 

// invoke a function
aCoolFunc()

NOTE: the 'function' keyword is what 
distinguishes a function declaration from 
a function invokation

- can run a function as many times as we want

* PARAMETERS AND ARGUMENTS IN A FUNCTION *

- can have as many arguments as you want

function myMessage(name) {
    console.log('hello ' + name + '!')
}

//can call a function with different parameter values
myMessage('Jack')
myMessage('Will')

let newUser = 'Velma'
myMessage(newUser)

---------------------------

function myMessage(firstName, lastName) {
    console.log('Hello, ' + firstName + ' ' + lastName)
}

/* the variables 'first' and 'last' don't
have to match the parameters from our 
myMessage function
*/

let bananas = 'John'
let oogabooga = 'Frett'
myMessage(bananas, oogabooga)

---------------------------

- we've been console.logging code in functions

/* the 'return' keyword will return us a value where
the function was invoked
*/

function addition (a, b) {
    let sum = a + b
    return sum
}

console.log(addition(7, 5))

// return is different from console.log
// console.log displays value in the console
// so addition(7,5) represents 12

let y = 5 + addition(7,5)
console.log(y) // returns 17

---------------------------

function isEven(x) {
    if(x % 2 === 0) {
        return true
    } else {
        return false
    }
}

console.log(isEven(555)) // return false
console.log(isEven(400)) // return true