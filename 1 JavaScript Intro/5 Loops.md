*** INTRO ***

Tidy Code Tips

--- Indentation ---
- Every codeblock should be indented
- Codeblocks begin and end with a curly brace

if(name === 'barry') {
    return 'hi there, barry!'
}
--- Variable Naming ---
- Use camelCase when defining variable names
- let myFavoritePlace = ‘FullStack’;
- Don’t use ambiguous variable names
- try to avoid something like: let x = 68;
- Use names that describe the value that they contain
- let currentTemp = 68;
- It’s ok to use short variable names as counters, like i in a for loop

----------------------------------------------

Loops

--- While loop ---

/*
A while loop requires three elements:
(1) the while keyword
(2) a conditional expression that evaluates to a boolean value
(3) a block of a code
*/

while (conditional) {
	// block of code
}

/* 
the block of code will run over & over as long as the condition
expressed evaluates to true
*/

let count = 3;

while (count >= 1) { // the count is greater than or equal to 1
    console.log(‘count is ’, count);
	count--; // decrement count. Will first get count to 2, and then stop running once 1 is 
printed out
}

----------

while (false) {
	console.log(‘this line of code will never run’);
}
----------

while (true) {
	console.log(‘this line will run forever’’);
	// (or until the machine running the code runs out of memory)
}

let count = 3;

//have to make sure the conditional is eventually false! Below is code that would show a while loop iterating forever

while (count >= 1) {
	console.log(‘count is ‘, count); //without the decrement count, this while loop will run 
forever since the count is just left to be assigned to value of 3

//the condition of count >= 1 never becomes false in this case
}

For loop
// a for loop requires 3 elements:
The for keyword
Three optional expressions
A block of code

for (initialization; conditional; final-expression (or some kind of change)) {
	//block of code
}

//the block of code will run over & over until the condition--the thing between the two semi-colons--evaluates to false

// the initialization is run first, and only once. It’s often used to define a counter variable

for (let i = 1; i  <= 3; i++) {
	console.log(‘i is ’, i);
}

// can loop in either direction 

for (let i = 5; i  >= 1; i--) {
	console.log(‘i is: ‘,  i);
}

// can increment by any number

for (let i = 100; i <= 300; i += 100) {
	console.log(‘i is: ‘ , i);
} 

//start i at 100. Test if i is less than or equal to 300. For each loop, increment i by 100

// use for loops to iterate through a string

let letters = ‘abcdefg’;

for (let i = 0; i < letters.length; i++) {
	let currentLetter = letters[i]
	console.log(currenLetter);
}

// use for loops to iterate through a string, BACKWARDS

let letters = ‘abcdefg’;

// init: let i = letters.length  - 1. The - 1 at the end of a length method will get the last character of a string
// cond: i >= 0
// final: i--

for (let i = letters.length - 1; i >= 0; i--) {
	let currentLetter = letters[i];
	console.log(currenLetter);
}

// can make the above for loop with a while loop:

let letters = ‘abcdefg’;

// init is outside the for loop
let j = letters.length - 1; // will start at the last character of the string

while (j >= 0) { // conditional
	let currentLetter = letters[j]; // codeblock
	console.log(currentLetter);
	j--; // final expression
}

Continue keyword

// the continue keyword will cause the loop to skip to the next iteration

for (let i = 1; i <= 5; i++) {
	if (i === 3) {
		continue; // will skip printing 3 to the console
	}
	console.log(‘i is’, i);
}

// the continue keyword also works with while loops

let count = 5;

while (count >= 1) {
	if (count % 2 === 0) { // if number is even (so has a remainder of 0)
	continue; // will skip printing even numbers to the console
}

console.log(‘count is ‘, count);
count--;
}

Break keyword

// the break keyword breaks out of the loop permanently

let myGrade = ‘A’;

while (true) {
    myGrade += ‘+’;
    
    if (myGrade.length === 3) { // put the break in a if statement
	    break;
    }
}

console.log(myGrade); // expect to see ‘A++’, since there are 3 characters

// the break keyword also works in for loops 

for (let i = 10; i >=1; i--) {
    console.log(‘i is ‘, i);

	if (i===7) { // put the break in a if statement
        break; // when i equals 7, it will print but go to the end of the for loop from here
		//notice that we will still see 7 printed on the console, since the console.log
		runs before the if statement
    }
}