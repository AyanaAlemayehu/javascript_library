# What is NPM?

# Understanding Node.js Modules

## What is a module?

A module is basically a JavaScript library which would contain a set of functions that you want to include in your code.

Node.js has many built-in modules that you can simply use without installing anything. A list of modules can be found [here](https://www.w3schools.com/nodejs/ref_modules.asp).

## Including modules in your own code

To use a module in your code, use the function `require()`.

<pre><code>var http = require('http')</code></pre>

The `require()` function reads a JavaScript file, executes it, and then returns the `exports` object. The `exports` keyword makes properties and methods available outside of the module file.

## Example

### Create a module that returns the current date and time.

<pre><code>exports.myDateTime = function () {
  return Date();
};</code></pre>

### Use this module in a Node.js file

<pre><code>var dt = require('./myfirstmodule');</code></pre>

We use the `./` here to locate the module because the module is located in the same file as the Node.js file.

## Sources

[W3Schools](https://www.w3schools.com/nodejs/nodejs_modules.asp)

[NodeJS](https://nodejs.org/en/knowledge/getting-started/what-is-require/)

# Creating index.js and package.json?

# Publishing and Installing?
