### Node.js
- A program that can run JavaScript files in the terminal.
https://nodejs.org.

### Run JavaScript using Node.js
`node greeting.js`
`node ./controllers/greetingTest.js`

### Named imports and exports
`import { } from ""`
`export function greeting(name)`

- Must use curly braces.
- Must use the exact module name.
- There can be multiple named exports in a single file. 
1. Make a greeting function that accepts a name and logs a greeting.
2. Import the greeting function and use it.
3. Run the module with `node` and observe the error.
4.  Or use relative path notation: `node ./controllers/greetingTest.js`

### Default imports and exports
`import sayHiTo from "../modules/greeting.js";`
`export default function greeting (name)`

- Does not use curly braces.
- Can use a different name than the module.
- Add the `default` keyword to the export.
- There can only be 1 default export per file.

### NPM
- Node Package Manager
- A program that comes with Node.js.
- Let's Node.js use modules.
- npm can manage dependencies.
- npm can (in one command line) install all the dependencies of a project.
- Also use to install code from other JavaScript programmers.
- https://npmjs.com

### How to configure Node.js for modules
- Initialize NPM.
- `npm init`
- Select the default options by pressing ENTER.
- VS Code creates the package.json file. 

### package.json{}
- Configuration file for Node.js.
- Installed node modules (external) are listed. 
- Must be initialized and installed fresh for every new project. 
1. Initialize npm for the project, using `npm init`, then select the default options by pressing ENTER.
2. Review JSON in package.json{}.
3. Add "type": "module" to package.json{}.
4. Run the greeting module.

### Require function
`var toNoCase = require('to-no-case')`
```javascript
const result = toNoCase("Hello World!");
```
`var camel = require('to-camel-case')`

- The old way of importing modules.
- Not compatible with web browsers even though it's JavaScript.
- Can be replaced with default import syntax: `import toNoCase from "to-no-case";`