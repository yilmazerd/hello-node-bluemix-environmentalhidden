bluemix-hello-node with hidden environmental variables
================================================================================

A "Hello World" server in node.js sample for Bluemix.
Follow the instructions on: https://github.com/IBM-Bluemix/node-helloworld
This project does the following modifications:
1) Creates an .env file add the following sample variables:
FOO = boo;
TOO = shoo;

2) Adds the following dependency in package.json (note that you might need to change the version of dotenv)
"dotenv": "^4.0.0",

3) Adds the following line in .gitignore
.env

4) Calls dotenv in server.js 
require('dotenv').config();

5) Calls the following function to reach the environmental variable in server.js
console.log(process.env.FOO)
