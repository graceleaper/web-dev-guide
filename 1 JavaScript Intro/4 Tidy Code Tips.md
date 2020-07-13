# Tidy Code Tips

## Indentation
- Codeblocks begin and end with a curly brace
- Every line inside a codeblock should be indented

```
if(name === 'barry') {
    return 'hi there, barry!'
}
```
## Variable Naming
- Use camelCase when defining variable names:
```
let myFavoritePlace = ‘The Buckley School’;
```
- Don’t use ambiguous variable names
- try to avoid something like: let x = 68;
- Use names that describe the value that they contain:
```
let currentTemp = 68;
```
- It’s ok to use short variable names as counters, like i in a for loop