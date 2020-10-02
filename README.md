# What is NPM?

NPM stands for Node Package Manager. It serves as a free package registry accessible to anyone, making it easier to share javascript packages with others. Users usually interact with NPM in two ways: as someone *downloading* a package and someone *publishing* a JavaScript package.

## Sources

[W3Schools](https://www.w3schools.com/whatis/whatis_npm.asp)

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

# Publishing and Installing

## Authentication
In order to publish a javascript package using NPM you need to first authenticate your NPM account in the command line. You can do this by using the command `npm login` which will prompt you for your login credentials. To test that you have successfully completed the authenticaiton you can use the command `npm whoami` and the command line should return your username if you have successfully logged in.

## Publishing
Once you have completed the authentication, in order to publish your package using NPM simply type the command `npm publish` into your command line.
Note: make sure you are in the correct directory and that you are using or rename your package a unique name because the publishing will not work if there is a package with an identicle name already on NPM.

## Installing
In order to install an existing package available through NPM simply create a new directory you want to house your files, use the command `npm init` and specify the details of the package you are creating, and then type the command `npm install package_name --save`. To see that you have properly installed the package use the `ls` command and the package name should be listed in the directory contents.

## Sources
Used [this](https://medium.com/the-andela-way/build-and-publish-your-first-npm-package-a4daf0e2431) article on how to build and publish your first NPM package as a reference source.