# Nodoc

First iteration / version of the nodoc block. Simplifying how to document code for Javascript and other languages if you want.

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
     
### Breakdown

```
// [Details regarding what method / function does]
//
// [Argument details, optional and required.]
// If you have both optional and required arguments you should denote required parameters like so:
//
// - **`Argument`** `Type` *Information*
//
// Otherwise:
// 
// - `Argument` `Type` *Information*
//
// [Example: (language)]
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

If you have required and optional parameters, the required arguments are to be wrapped with bold markup.

```
// … 
// - **`Argument`** `Type` *Information detailing argument*
// - `callback` `Function` *Invoked after a result has been calculated*
// … 
```

#### Outputs

- **`Argument`** `Type` *Information detailing argument*
- `callback` `Function` *Invoked after a result has been calculated*

## License & Copyright

MIT

2013 Nijiko Yonskai <nijikokun@gmail.com>
