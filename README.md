# tslint-json

A sane [tslint](https://palantir.github.io/tslint) style.

These represent sane defaults for a typescript project (file an issue if found insane).
The aim of this project is to keep a solid working style for each tslint version,
tagged to keep consistancy.


## Rules
[See tslint rules for additional information.](https://palantir.github.io/tslint/rules/)


### array-type
```json
    "array-type": [true, "generic"]
```

Requires using either `T[]` or `Array` for arrays.

All objects/classes to be referenced capcase.

Example 
```typescript
public test(testSteps: Array<Array<string>>, testName: string): void {}
```


### arrow-parens
```json
   "arrow-parens": [true, "ban-single-arg-parens"]
```

Requires parentheses around the parameters of arrow function definitions.

If `ban-single-arg-parens` is specified, then arrow functions with one parameter must not have parentheses if removing them is allowed by TypeScript.


### class-name: Boolean
```json
   "class-name": true
```

Enforce PascalCased class and interface names. Makes it easy to differentitate classes from regular variables at a glance.


### cyclomatic-complexity: Boolean | Array
```json
    "cyclomatic-complexity": [true, 3]
```

Complexity based on statements and expressions such as * `catch` * `if` and `? :` * `||` and `&&` due to short-circuit evaluation * `for`, `for in` and `for of` loops * `while` and `do while` loops.
3 is sane. 4, insane.


### comment-format: Array
```json
    "comment-format": [true, "check-space"]
```

Enforce formatting rules for single-line comments.


### eofline: Boolean
```json
    "eofline": true
```

Ensure the file ends with a newline.


### indent: Array
```json
    "indent": [true, "spaces"]
```

Enforce indentation with spaces.


### jsdoc-format: Boolean
```json
    "jsdoc-format": true
```

Enforce basic format rules for JSDoc comments.


### max-classes-per-file: Array
```json
    "max-classes-per-file": [true, 1]
```

Ensures that files have a single responsibility so that that classes each exist in their own files and 1 per file keeps everyone sane. Should also name the file the `[classname].ts`.


### max-file-line-count: Array
```json
    "max-file-line-count": [true, 300]
```

Ensure a file stays under a certain line count. Most people don't like scrolling more than 300.


### no-default-export: Booleanhighlighter symantec
```json
    "no-default-export": true
```

Be original, name your import something other than `default`.


### no-duplicate-variable: Array
```json
    "no-duplicate-variable": [true, 1]
```

There’s no good reason to have a duplicate variable declaration.


### no-parameter-properties: Array
```json
    "no-parameter-properties": true
```

More verbose and explicit but easier to understand. [Example](https://github.com/Wintellect/intro-to-typescript/blob/master/classes-parameter-properties.ts)


### no-eval: Boolean
```json
    "no-eval": true
```

Eval is unsafe. Try `.call()` or some other method to achieve your goals.


### no-internal-module: Boolean
```json
    "no-internal-module": true
```

Use the `namespace` keyword and not `module`.


### no-trailing-whitespace: Array
```json
    "no-trailing-whitespace": true
```

No trailing whitespace.


### no-unsafe-finally: Boolean
```json
    "no-unsafe-finally": true
```

Disallows control flow statements, such as `return`, `continue`, `break` and `throws` in `finally` blocks.


### no-var-keyword: Boolean
```json
    "no-var-keyword": true
```

Use `let` or `const` instead of `var`.


### object-literal-key-quotes: Array
```json
    "object-literal-key-quotes": [true, "always"]
```

Property names should always be quoted.


### object-literal-shorthand: Boolean
```json
    "object-literal-shorthand": true
```

Enforce use of ES6 object literal shorthand when possible.


### object-literal-sort-keys: Boolean
```json
    "object-literal-sort-keys": true
```

Require keys in object literals to be sorted alphabetically.


### one-line: Array
```json
    "one-line": [
        true,
        "check-open-brace",
        "check-whitespace"
    ],
```

Require the open brace and whitespace to be on the same line as the expression preceding them.


### ordered-imports: Array
```json
    "ordered-imports": [
        true,
        {
            "import-sources-order": "lowercase-last",
            "named-imports-order": "lowercase-first"
        }
    ],
```

Require that import statements be alphabetized.


### one-variable-per-declaration: Boolean
```json
    "one-variable-per-declaration": [true, "ignore-for-loop"]
```

No multiline declaration unless in a `for` loop.

