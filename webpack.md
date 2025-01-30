# Webpack
### Node Modules
- A node module that allows other node modules to be used in the browser
- Packs code into 1 file where `exports`/`imports`/`requires` are not necessary

### Package installation
-  Needs 2 packages (or node modules) so it can run in the terminal
```javascript
1.View the webpack website https://webpack.js.org/
2. `npm install webpack webpack-cli`
```
- What webpack does: Bundles your files together and categorizes accordingly
- `webpack` -  The main module with functions and classes
- `webpack-cli` - A controller that allows webpack to be used in the command line

### Running Webpack
### npx: node package eXecute
`npx webpack`
- runs node modules in the terminal
- comes bundled with NPM
- This command expects the following folder structure:
    - `src` folder in `index.js` file inside of it
### Folder Structure
```
>src
    - index.js
```
- The packed (or bundled) file is generated in the `dist` folder as `main. js`
- Connect `main. js` to the HTML file instead of the original module
`<script src="./dist/main.js" type="module"></script>`