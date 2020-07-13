# Loops

## While Loops

- A while loop requires three elements:
	- The `while` keyword
	- A conditional expression that evaluates to a boolean value
	- A block of a code

```
while (conditional that evaluates to a boolean) {
	// block of code
}
```
- In a while loop, the block of code will run over and over as long as the condition expressed evaluates to true

```
let count = 3;

while (count >= 1) { // while count is greater than or equal to 1...
    console.log(‘count is ’, count);
	count--; // decrement count. Will first get count to 2, and then stop running once 1 is 
printed out
}
```

```
while (false) {
	console.log(‘this line of code will never run’);
}
```

```
while (true) {
	console.log(‘this line will run forever’’);
	// (or until the machine running the code runs out of memory)
}
```

```
let count = 3;

// have to make sure the conditional in the while loop is eventually false! Below is code that would show a while loop iterating forever

while (count >= 1) {
	console.log(‘count is ‘, count);
	/*
	without the decrement count, this while loop will run forever since the count is just left to be assigned to value of 3
	*/

// the condition of count >= 1 never becomes false in this case
}
```

## For Loops
- A for loop requires 3 elements:
	- The `for` keyword
	- Three optional expressions
	- A block of code

```
for (initialization; conditional; final-expression (or some kind of change)) {
	//block of code
}
```

- The block of code will run over and over until the condition–the expression between the two semi-colons–evaluates to false

- The initialization is run first, and only once. It’s often used to define a counter variable

```
for (let i = 1; i <= 3; i++) {
	console.log(‘i is ’, i);
}
```

- You can loop in either direction. So you can decrement:

```
for (let i = 5; i >= 1; i--) {
	console.log(‘i is: ‘,  i);
}
```

- You can increment by any number:

```
for (let i = 100; i <= 300; i += 100) {
	console.log(‘i is: ‘, i);
}

/*
start i at 100. Test if i is less than or equal to 300. For each loop, increment i by 100
*/
```

- Use for loops to iterate through a string:

```
let letters = ‘abcdefg’;

for (let i = 0; i < letters.length; i++) {
	let currentLetter = letters[i]
	console.log(currenLetter);
}
```

- Use for loops to iterate through a string, BACKWARDS:

```
let letters = ‘abcdefg’;

// initilization: let i = letters.length  - 1. The - 1 at the end of a length method will get the last character of a string
// condition: i >= 0
// final: i--

for (let i = letters.length - 1; i >= 0; i--) {
	let currentLetter = letters[i];
	console.log(currenLetter);
}
```

- Can make the above for loop with a while loop:

```
let letters = ‘abcdefg’;

// init is outside the for loop
let j = letters.length - 1; // will start at the last character of the string

while (j >= 0) { // conditional
	let currentLetter = letters[j]; // codeblock
	console.log(currentLetter);
	j--; // final expression
}
```

## Continue keyword

- The `continue` keyword will cause the loop to skip to the next iteration

```
for (let i = 1; i <= 5; i++) {
	if (i === 3) {
		continue; // will skip printing 3 to the console
	}
	console.log(‘i is’, i);
}
```

- The `continue` keyword also works with while loops:

```
let count = 5;

while (count >= 1) {
	// if number is even (so has a remainder of 0)...
	if (count % 2 === 0) {
		// ... will skip printing even numbers to the console
		continue;
	}
console.log(‘count is ‘, count);
count--;
}
```

## Break keyword

- The `break` keyword breaks out of the loop permanently:

```
let myGrade = ‘A’;

while (true) {
    myGrade += ‘+’;
    
    if (myGrade.length === 3) { // put the break in a if statement
	    break;
    }
}

console.log(myGrade); // expect to see ‘A++’, since there are 3 characters
```

- The `break` keyword also works in for loops :

```
for (let i = 10; i >=1; i--) {
    console.log(‘i is ‘, i);

	if (i===7) { // put the break in a if statement
        break; // when i equals 7, it will print but go to the end of the for loop from here
		
		//notice that we will still see 7 printed on the console, since the console.log
		runs before the if statement
    }
}
```