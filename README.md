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
```json
    public test(testSteps: Array<Array<string>>, testName: string): void {}
```


### arrow-parens
```json
   "arrow-parens": [true]
```

Requires parentheses around the parameters of arrow function definitions.


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
    "max-file-line-count": [true, 100]
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
    ]
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
    ]
```

Require that import statements be alphabetized.


### one-variable-per-declaration: Boolean
```json
    "one-variable-per-declaration": [true, "ignore-for-loop"]
```

No multiline declaration unless in a `for` loop.


### quotemark: Array
```json
    "one-variable-per-declaration": [true, "double"]
```

Require double quotes for string literals.


### semicolon: Array
```json
    "semicolon": [
        true,
        "always"
    ]
```

Enforce semicolons at the end of every statement including bound class methods and
interfaces.


### trailing-comma: Array
```json
    "trailing-comma": [
        false,
        {
            "multiline": "never",
            "singleline": "never"
        }
    ]
```

Disallow trailing commas in array and object literals, destructuring assignments,
function and tuple typings, named imports and function parameters.


### triple-equals: Boolean
```json
    "triple-equals": true
```

Requires `===` and `!==`, no exceptions.


### typedef-whitespace: Array
```json
    "typedef-whitespace": [
        true,
        {
            "call-signature": "nospace",
            "index-signature": "nospace",
            "parameter": "nospace",
            "property-declaration": "nospace",
            "variable-declaration": "nospace"
        }
    ]
```

No space is required before the colon in a type specifier.



### variable-name: Array
```json
    "variable-name": [
        true,
        "check-format",
        "allow-leading-underscore",
        "allow-trailing-underscore",
        "allow-pascal-case",
        "ban-keywords"
    ]
```

Checks variable names for various errors.
 - `"check-format"`: allow only camelCased or `UPPER_CASED` variable names
   - `"allow-leading-underscore"`: allow underscores at the beginning (only has an effect if `“check-format”` specified)
   - `"allow-trailing-underscore"`: allow underscores at the end. (only has an effect if `“check-format”` specified)
   - `"allow-pascal-case"`: allow PascalCase in addtion to camelCase.
 - `"ban-keywords"`: Do not allow the use of certain TypeScript keywords (`any`, `Number`, `number`, `String`, `string`, `Boolean`, `boolean`, `undefined`) as variable or parameter names.


### whitespace: Array
```json
    "whitespace": [
        true,
        "check-branch",
        "check-decl",
        "check-operator",
        "check-module",
        "check-separator",
        "check-type",
        "check-typecast"
    ]
```

Enforce whitespace style conventions.
 - `"check-branch"` check branching statements (`if/else/for/while`) are followed by whitespace.
 - `"check-decl"` check that variable declarations have whitespace around the equals token.
 - `"check-operator"` check for whitespace around operator tokens.
 - `"check-module"` check for whitespace in import & export statements.
 - `"check-separator"` check for whitespace after separator tokens (`,/;`).
 - `"check-type"` check for whitespace before a variable type specification.
 - `"check-typecast"` check for whitespace between a typecast and its target.
 - `"check-preblock"` check for whitespace before the opening brace of a block
