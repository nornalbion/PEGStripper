Aloha
=====

Hello there! This is a README file for when you want to learn how to use PEGStripper and also for telling you what it is!

I'm really bored so I've decided to write this in the style of a small child, who just learned what conjunctions are and I hope you like it!

So anyway hello! PEGStripper is a JavaScript program what is for node.js and it is a program what is good for when you have PEG.js files what you don't want to have JavaScripts in. It might work in other PEG languages if they have similar syntax (possibly C/Java?) but I don't guarantee anything.

Here is how to install it by typing words into boxes:

	$ npm install pegstripper

Here is what you type in to use it when you are typing what you type into a terminal or command line:

	$ pegstripper [-d | --debug] [-s | --strip-comments] [-o file | --output file] file
	$ pegstripper [-h | --help]

In the normal times PEGstripper outputs output to standard output.

The options!
============

`-h` / `--help`
---------------

I think you already know what this will do.

`-d` / `--debug`
------------

`--debug` makes it so that when PEGStripper outputs a character, what it actually outputs is a JSON object on its own line loaded with the lexer's state. Whoa!

`-s` / `--strip-comments`
---------------------

When you want for your outputted output to not have comments in it then you can type `-s` to make it so that what I just said.

`-o file` / `--output file`
--------------------------

`-o` makes it so that instead of outputting output to standard output, output is outputted to the file specified by `--output`!

Using PEGStripper as a library
==============================

I don't know why you would do this

	$ npm install pegstripper
	$ cat example.js
	var pegstrip = require('pegstripper'), fs = require('fs');
	console.log(pegstrip(fs.readFileSync('example.pegjs'));

	$ cat example.pegjs
	string = "'" str:string "'" { return str; }

	$ node example.js
	string = "'" str:string "'" 
	


What if it breaks?
==================

[Open an issue](http://github.com/telyn/PEGStripper.git)

I hate your readme so much
==========================

It doesn't have to be that way. Rewrite it and send me a pull request.
