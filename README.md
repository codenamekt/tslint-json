# tslint-json

A sane [tslint](https://palantir.github.io/tslint) style.

These represent sane defaults for a typescript project (file an issue if found insane).
The aim of this project is to keep a solid working style for each tslint version,
tagged to keep consistancy.


## { "rules": {
[See tslint rules](https://palantir.github.io/tslint/rules/)


### array-type
```json
{
    "array-type": [true, "generic"]
}
```

Requires using either `T[]` or `Array` for arrays.

All objects/classes to be referenced capcase.

Example 
```typescript
public test(testSteps: Array<Array<string>>, testName: string): void {}
```


### arrow-parens
```json
{
   "arrow-parens": [true, "ban-single-arg-parens"],
}
```

Requires parentheses around the parameters of arrow function definitions.

If `ban-single-arg-parens` is specified, then arrow functions with one parameter must not have parentheses if removing them is allowed by TypeScript.


### class-name: Boolean
```json
{
   "class-name": true
}
```

Enforces PascalCased class and interface names. Makes it easy to differentitate classes from regular variables at a glance.


### cyclomatic-complexity: Boolean | Array
```json
{
    "cyclomatic-complexity": [true, 3]
}
```

Complexity based on statements and expressions such as * `catch` * `if` and `? :` * `||` and `&&` due to short-circuit evaluation * `for`, `for in` and `for of` loops * `while` and `do while` loops.


### comment-format: Array
```json
{
    "comment-format": [true, "check-space"]
}
```

Enforces formatting rules for single-line comments.


### eofline: Boolean
```json
{
    "eofline": true
}
```

Ensures the file ends with a newline.


### indent: Array
```json
{
    "indent": [true, "spaces"],
}
```

Enforces indentation with tabs or spaces.


### jsdoc-format: Boolean
```json
{
    "jsdoc-format": true,
}
```
Enforces basic format rules for JSDoc comments.
