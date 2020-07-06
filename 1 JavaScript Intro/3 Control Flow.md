# What is control flow?

* Code runs from top to bottom

```
let myNum = 5;
console.log(myNum);
```

* But what we if we want certain lines to run out of order?
* Control flow enables us to change the order in which our code runs

* The "if statement" is a JavaScript feature that allows us to affect
control flow

* The if statement starts with 'if' keyword then, two parens around expression
curly brackets surrounding lines of code to run the code around curly braces will only run if the expression is true

```
if (true) {
    console.log('n the if')
}
```

```
console.log('hi there')
```

```
if (false) {
    console.log('bye, friend')
}
```

```
if (true) {
    console.log('see you later')
}
```

```
const classAvg = 75;
```

```
if (classAvg === 75) {
    console.log('wow, great job class!')
}
```

```
if (classAvg === 60) {
    console.log('how disappointing, class')
}
```

## if / else statement

* Code in an else block will run only if the
expression in the if evaluates to false

* Would not expect the code in the if statement to run:

```
if (false) {
    console.log('this is the if clause')
} else {
    console.log('this is the else clause')
}
```

```
const student = 'Jerry' 

if (student === 'Jerry') {
    console.log('this is the if clause')
} else {
    console.log('this is the else clause')
}
```

* Example of 'else if' clause:

```
const name = 'Ron';

if (name === 'Ruby') {
    console.log('Hi there, Ruby!')
} else if (name === 'Roger') {
    console.log('Hi there, Roger!')
} else {
    console.log('Hi there, friend!')
}
```

## Logical Operators

* && is the logical 'and' OPERATORS
* Place && between two values and see if the 2 values are BOTH true

```
if (true && true) {
    console.log('both guys are truthful')
}
```

```
if (true && false) {
    console.log('one of these guys is truthful')
}
```

```
const teacher = 'Mr. Smith'
const student = 'Larry Davies'

if (teacher === 'Mr. Smith && student === 'Larry Davies') {
    console.log('everyone is present!')
}
```

* Block of code in the next if statement will never run since
we declared variable teacher as 'Mr. Smith' earlier – NOT 'Mr. Adams'

```
if (teacher === 'Mr. Adams && student === 'Larry Davies') {
    console.log('everyone is present!')
}
```

* || is the logical 'or' operator
* Returns true if either one of the values on either side of || is true

```
if (false || true) {
    console.log('everything is true')
}
```

* Below code block in if statement won't execute:

```
if (false || false) {
    console.log('everything is false')
}
```

```
const teacher = 'Mr. Smith'
const student = 'Larry Davies'

if (teacher === 'Mr. Adams || student === 'Larry Davies') {
    console.log('we have people in the room!')
}
```

* If _both_ values on either side of the or operator is false, then code block inside of if statement will never run

```
if (teacher === 'Mr. Adams || student === 'Sam Bills') {
    console.log('we have people in the room!')
}
```