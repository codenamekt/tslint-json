# tslint-json

A sane [tslint](https://palantir.github.io/tslint) configuration.

These represent sane defaults for a typescript project (file an issue if found insane).
The aim of this project is to keep a solid working config for each tslint version,
tagged to keep consistancy.

## { "rules": {
[See tslint rules](https://palantir.github.io/tslint/rules/)

```
{
    "array-type": [true, "generic"]
}
```

Requires using either `T[]` or `Array` for arrays.

All objects/classes to be referenced capcase.

Example ``

```
{
   "arrow-parens": [true, "ban-single-arg-parens"],
}
```

Requires parentheses around the parameters of arrow function definitions.

If `ban-single-arg-parens` is specified, then arrow functions with one parameter must not have parentheses if removing them is allowed by TypeScript.

```
{
    "array-type": [true, "generic"]
}
```

```
{
    "array-type": [true, "generic"]
}
```

```
{
    "array-type": [true, "generic"]
}
```

```
{
    "array-type": [true, "generic"]
}
```