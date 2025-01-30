### Function Hoisting
- JavaScript invisibly brings function definitions to the top
- Functions can be called before they are defined in a file

### Object Oriented Programming
- Create objects that bundle related data and functions together
- The keywords `class`, `new`, and `this` are used to achieve OOP

### Folder Structure
```
> controllers
> modules
> utils
```
- `modules` Contains functions specific to the project
- `utils` Contains functions that can be used by other projects
- `controllers` Contains functions that control the flow of how modules are used. Handlers usually go into controllers folder
- Usually only 1 function or class per file

### MODULE ERRORS
 ```
 @ GET
http://localhost:8081/utils/output
net:: ERR_ABORTED 404 (Not Found)
 ```   
  - file name is incorrect. 
  - to correct the error: must add `.js` to the end of the `import` statement
  - correct filepath: import {output} from "./output.js"

### AUTOMATICALLY IMPORT
1. Open the `module` file
2. Open the file that will import the `module`
3. Start typing the `module` name
4. Select the `module` from the popup list  

### Property chaining for objects
`const cylinderCount = car.components.engine.parts.cylinders.count;`

- Using object dot notation, properties can be chained together.
- Access deeper property levels with just one line.

        <button onclick="propertyChainingExample()">Property Chaining</button><br><br>
        <output id="propertyChainingTag"></output>
        
function propertyChainingExample() {
    const myCar = 1
        components: {  
            engine: {  
                parts: { 
                    cylinders: { 
                        count: 4
                    }, 
                }, 
            }, 
        } ,  
        const cylinderCount = car.components. engine.parts.cylinders.count;
        output (cylinderCount, "propertyChainingTag", false);
}


### Item chaining for arrays
`const value = myArrays[0][2];`
- Using array notation, items can be chained together.
- Access deeper array levels with just one line.

  <button onclick="itemChainingExample()">Property Chaining</button><br><br>
        <output id="itemChainingTag"></output>
        
function arrayItemChaining() {
    myArrays[
        [1,2,3],
        [4,5,6],
        ["A","B","C"]
    ];
    const value = myArrays[0][2]; 
    output(value, "itemChainingTag", false);
} 
 
 ### Property and item chaining
`const value = event.target[0].value;`

- Using array and object dot notation, items and properties can be chained together.
- Access deeper array and object levels with just one line.

### Node.js
- A program that can run JavaScript files in the terminal
- JavaScript for the back end (used by terminal)
- slightly different from JavaScript for the front end (used by website)

```
1. Go to https://nodejs.org
2. Download Node.js
3. Install Node.js with default options
```
### Named exports/imports
`import { greeting } from "./modules/greeting.js";`
- Must use curly braces
- Must use the exact module name
```
1. Make a greeting function that accepts a name and logs a greeting
2. Import the greeting function and use it
3. Run the module with node and observe the error
```
### NPM
- Node Package Manager
- program that comes with node.js
- allows Node.js to use modules

### How to configure Node.js for modules
`{} package.json`
- Configuration file for Node.js
1. Initialize NPM for the project
  - `npm init`
  - Select the default options by pressing Enter
2. Review JSON in package.json
3. Add "type": "module" to package.json
4. Run the greeting module

### require Function
`var toNoCase = require('to-no-case')`
- The old way of importing modules
- Not compatible with web browsers
- Can be replaced with default import syntax

Node Package Manager
```javascript
1. Install `npm install to-no-case` package
2. Import with `default` import syntax
3. Note the path difference
4. Use `toNoCase` and log the results
```
### Node Modules
- Node modules are resusable code that can be installed with NPM
```javascript
- Install and use `npm install to-camel-case` package 
- Install and use `npm install to-space-case` package
```

### Node modules
`>npm install to-no-case`
`>npm install to-camel-case`
`>npm install to-camel-case`

- Reusable code that can be installed with NPM.
- NPM commands start with `npm`. 
- Add the `install` command to install a module from npmjs.org.
- May not be compatible with the browser. 

### Internal modules
`import sayHiTo from "../modules/greeting.js";`

- Modules that were created in the project.
- Must be imported with relative path notation. 

### External modules
`import toNoCase from "to-no-case";`

- Modules that were installed from NPM.
- Must be imported with their package name.

