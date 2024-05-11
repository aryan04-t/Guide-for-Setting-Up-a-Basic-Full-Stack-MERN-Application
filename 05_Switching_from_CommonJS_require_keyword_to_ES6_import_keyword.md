# Switch from CommonJS require to ES6 import: 


- ES6 was released in 2015 and that introduced ` "import" ` and ` "export" ` keywords 
- Before ES6 was released, we used ` "require" ` keyword for importing the packages which we installed from npm 
- But in ES6 a new keyword "import" was introduced for importing packages into your code 
- require keyword is not obsolete it can still be used but using "import" keyword is preferred by a lot of developers as it has its own benefits and it is a new better keyword than the "require" keyword 
- But because the "require" keyword is an old keyword and it doesn't really have significant demerits that's why it is still widely accepted and the old code base obviously still have "require" keyword in them 
- require keyword can be used directly in app.js once the package.json is initialized, because the default script type for package.json is "commonjs", but for using import keyword, you have to go to your package.json file of Backend and there just below the "scripts" key-value pair you have to add this below mentioned key-value pair so that you can start using import keyword instead of require keyword when you're coding your Backend 
> type : "module"  
- "type" : "module" indicates that the script should be considered a "JavaScript module", which is by-default "commonjs" 
- I will use "import" keyword, because in my Vite + React frontend application the import keyword is used and I will like to keep my code base consistent and up-to date with the newer versions of JS 



## In our Backend's app.js before we used to import packages like this by using the Common JS "require" keyword: 

```
const express = require('express'); 
const dotenv = require('dotenv'); 
```


## But now we can now use "import" keyword of ES6 for importing packages: 

```
import express from 'express'; 
import dotenv from 'dotenv'; 

```



# Saving files with .mjs extension when we use "JavaScript Modules" feature which was introduced in ECMAScript 6: 

- When we used to use require keyword, our file's name was saved with .js file extension, like app.js and here "js stands for JavaScript, also known as Common JavaScript" 
- But when you start using import keyword by defining the script type as module in the package.json then its recommended to save files using .mjs extension 
- .mjs stands for "Modular JavaScript", this a file extension for JavaScript files that use the ECMAScript module format. 
- ECMAScript modules are a newer way to organize JavaScript code into smaller, reusable components. They are different from the older CommonJS module format, which is still widely used. 
- The use of .mjs file extension is not mandatory for ESM (ECMAScript Module) files, but it is often used to indicate that a JavaScript file uses the ESM format. This can be helpful for developers who are working with both ESM and CommonJS modules in the same project. 
- But even if you keep the file's extension as .js, your code will still run fine without any errors (At least till this date when I am documenting all this, it works. Today's Date is: 11th May 2024)



## * Note: 

- If you decide to rename your file from ` app.js ` to ` app.mjs ` then don't forget to update the "server" script and entry point of your backend application, the "main" key-value pair in the Backend's package.json file is where we have defined the entry point of your Backend 
- And once you update the package.json and rename ` app.js ` to ` app.mjs `, relaunch your backend by terminating nodemon and again running the "npm run server" command in the terminal 
- In Node.js, using both `require` and `import` keywords concurrently is prohibited 



# There are only 3 major differences between Nodejs "require" keyword and ES6 "import" keyword: 

| Node.js `require`                                        | ES6 `import` and `export`                                 |
|----------------------------------------------------------|------------------------------------------------------------|
| Require is Non-lexical, it stays where it has been put in the file. | Import is lexical, it gets sorted to the top of the file. |
| It can be called at any time and place in the program.  | It can’t be called conditionally, it always run in the beginning of the file. |
| If you want to use require module then you have to save file with '.js' extension. | If you want to use import keyword then you have to add key-value pair "type" : "module" in your package.json file and you have to save your '.js' files with '.mjs' extension wherever you are using ES6 import keyword. (but we know that saving them with .mjs is optional at least as of today, today's date is 11th May 2024, and right now time is: 11:12 P.M. IST) |



# Reference Cited: 

- GeeksForGeeks (Difference between Node require and ES6 import and export): 
https://www.geeksforgeeks.org/difference-between-node-js-require-and-es6-import-and-export/ 

- StackOverflow (Why is 'type: module' in package.json file?): 
https://stackoverflow.com/questions/61401475/why-is-type-module-in-package-json-file 

- W3Schools (JavaScript ES6): 
https://www.w3schools.com/js/js_es6.asp 

- Wikipedia (ECMAScript): 
https://en.wikipedia.org/wiki/ECMAScript 