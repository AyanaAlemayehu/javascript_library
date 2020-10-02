# What is NPM?

NPM stands for Node Package Manager. It serves as a free package registry accessible to anyone, making it easier to share javascript packages with others. Users usually interact with NPM in two ways: as someone *downloading* a package and someone *publishing* a JavaScript package.

## Sources

[W3Schools](https://www.w3schools.com/whatis/whatis_npm.asp)

[Medium](https://medium.com/the-andela-way/build-and-publish-your-first-npm-package-a4daf0e2431)

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

# Creating index.js and package.json
To build an NPM package, you'll need to:
1. Download and [install](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) npm and Node.js. 
2. Create a project directory and initialize npm in the Terminal.
3. Answer the prompted questions about your project in the Terminal. This will create a [`package.json`](https://docs.npmjs.com/creating-a-package-json-file) file, which is **crucial** for creating and publishing your NPM package. 
4. Create a new .js file with a name in front of the "main: " attribute of your `package.json` file. 
```
version: "1.0.0"
description: ""
main: "index.js"
```
5. Write your JS code in that file.
6. Add the export statement at the end of your code. 
```
function yourFunction (){
    ...
}
module.exports=yourFunction; 
``` 
7. You're ready to publish your package!

# Publishing and Installing
