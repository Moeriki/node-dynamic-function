# node-dynamic-function

Easily create functions with dynamic name and length. This is useful for wrapping functions without f'ing up their name and length.

[![Build Status](https://travis-ci.org/Moeriki/dynamic-function.svg?branch=master)](https://travis-ci.org/Moeriki/dynamic-function) [![Coverage Status](https://coveralls.io/repos/github/Moeriki/dynamic-function/badge.svg?branch=master)](https://coveralls.io/github/Moeriki/dynamic-function?branch=master) [![Known Vulnerabilities](https://snyk.io/test/github/moeriki/dynamic-function/badge.svg)](https://snyk.io/test/github/moeriki/dynamic-function) [![dependencies Status](https://david-dm.org/moeriki/dynamic-function/status.svg)](https://david-dm.org/moeriki/dynamic-function) [![Downloads](http://img.shields.io/npm/dm/dynamic-function.svg?style=flat)](https://www.npmjs.org/package/dynamic-function)

---

## Install

```sh
npm install --save dynamic-function
```

## Usage  

```javascript
const dynamicFunction = require('dynamic-function');

function originalFunction(originalArg, originalArg) {
    //
}

const wrappedFunction = dynamicFunction(originalFunction, {
  name: originalFunction.name,
  length: originalFunction.length,
});

console.log(wrappedFunction.name);   // logs 'originalFunction'
console.log(wrappedFunction.length); // logs 2
```
