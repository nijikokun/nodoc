# Nodoc

> Version 0.2

Simplifying how to document code for Javascript and other languages if you want.

***

### Basics

Here is our test code:

```
function equalsIgnoreCase (a, b) {
  return (a == b) ? true : (
    (!b.isEmpty()) && 
    (b.length == a.length) && 
    (a.toLowerCase() == b.toLowerCase())
  );
}
```

1. Single line comment notation only unless language does not support this notation.
2. Markdown is to be assumed as the parsing language.

An example nodoc block for this would resemble:

```
// Compares two strings for equality ignoring case sensitivity.
//
// - `a` `String` *Value to be compared against.*
// - `b` `String` *Value used for comparing against.*
//
// Example: (javascript)
//
//     // returns true
//     console.log(equalsIgnoreCase("hello World", "hello world"));
//
```

#### Github Flavoured Output

Compares two strings for equality ignoring case sensitivity.

- `a` `String` *Value to be compared against.*
- `b` `String` *Value used for comparing against.*

Example:

```javascript
     // returns true
     console.log(equalsIgnoreCase("hello World", "hello world"));
```

#### Raw Output

Compares two strings for equality ignoring case sensitivity.

- `a` `String` *Value to be compared against.*
- `b` `String` *Value used for comparing against.*

Example: (javascript)

     // returns true
     console.log(equalsIgnoreCase("hello World", "hello world"));
     
## Breakdown

```
// [Details regarding what method / function does]
//
// [Argument details list]
//
// [Example: (language)] - Optional Section
// [… code indented by four spaces …]
//
```


## Types Enum for Javascript

- `Mixed` *Can be a variety, explain upon necessity.*
- `Object`
- `Array`
- `Function`
- `String`
- `Number`
- `Boolean`
- `Date`
- `RegExp`
- `Null`
- `Undefined`
- `NaN`

## Extra Details

### Nest Information

Instead of having argument details and information on the same line, you can nest it below to keep readability a little higher.

```
// …
// - `Argument` `Type`
//   *Information regarding argument can go here*
// …
```

### Object Argument Information

How to document out an options or `Object` argument on a method or function:

```
// …
// - `options` `Object` *Information about Options Object*
//     - `Argument` `Type` *Information details regarding Argument*
//     - …
// - `callback` `Function` *Information about Another Argument*
// …
```

### Required and Optional

If you have required and optional parameters, the importance should be wrapped in bold & italics underscore syntax. You can choose either to do this with `Required` or `Optional` and it should like like so: `___Optional___`

***

**Note:** Originally this was meant to be a simple wrapping the argument code snippet with bold syntax, however github does not support bolding inline code snippets.

***

```
// … 
// - `Argument` `Type` ___Required___ *Information detailing argument*
// - `callback` `Function` *Invoked after a result has been calculated*
// … 
```

#### Outputs

- `Argument` `Type` ___Required___ *Information detailing argument*
- `callback` `Function` *Invoked after a result has been calculated*
