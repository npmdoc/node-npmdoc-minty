# api documentation for  [minty (v0.5.10)](https://www.mintyjs.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-minty.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-minty) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-minty.svg)](https://travis-ci.org/npmdoc/node-npmdoc-minty)
#### Node process visualization

[![NPM](https://nodei.co/npm/minty.png?downloads=true)](https://www.npmjs.com/package/minty)

[![apidoc](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-minty_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-minty/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ted Zilist",
        "email": "tzilist@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/lumpy-turnips/minty/issues"
    },
    "dependencies": {
        "app-root-path": "^1.0.0",
        "decomment": "^0.8.6",
        "esprima": "^2.7.2",
        "esquery": "^0.4.0",
        "eval": "^0.1.1",
        "jquery": "^2.2.2",
        "json-stringify-safe": "^5.0.1"
    },
    "description": "Node process visualization",
    "devDependencies": {
        "colortape": "^0.1.1",
        "coveralls": "^2.11.9",
        "eslint": "^2.5.0",
        "eslint-config-airbnb": "^6.2.0",
        "eslint-plugin-react": "^4.2.3",
        "expect": "^1.16.0",
        "istanbul": "^0.4.2",
        "mocha": "^2.4.5",
        "sinon": "^1.17.3",
        "tape": "^4.5.1",
        "zombie": "^4.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "b27569eae3487d11c45dd56c7eaf3393d7f2dd70",
        "tarball": "https://registry.npmjs.org/minty/-/minty-0.5.10.tgz"
    },
    "gitHead": "3d09132c6725e74aafd7fdd159fd2c072b0feaf1",
    "homepage": "https://www.mintyjs.com",
    "keywords": [
        "visualization",
        "node",
        "minty",
        "mintyjs",
        "tutor"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "angieyeh",
            "email": "angieyeh24@gmail.com"
        },
        {
            "name": "kaizendad",
            "email": "wade@wadearmstrong.com"
        },
        {
            "name": "tzilist",
            "email": "tzilist@gmail.com"
        }
    ],
    "name": "minty",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/lumpy-turnips/minty.git"
    },
    "scripts": {
        "anonfunctest": "node ./test/backend/test-anonFunc.js | colortape",
        "lineruletest": "node ./test/backend/test-createLR.js | colortape",
        "test": "mocha ./test/backend | colortape",
        "test-travis": "./node_modules/istanbul/lib/cli.js cover ./node_modules/mocha/bin/_mocha -- -R spec ./test/backend",
        "zombie": "mocha --timeout 5000 test/front-end-test.js"
    },
    "version": "0.5.10"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module minty](#apidoc.module.minty)
1.  [function <span class="apidocSignatureSpan">minty.</span>file (path)](#apidoc.element.minty.file)
1.  [function <span class="apidocSignatureSpan">minty.</span>wrap (func)](#apidoc.element.minty.wrap)
1.  object <span class="apidocSignatureSpan">minty.</span>createLineRules
1.  object <span class="apidocSignatureSpan">minty.</span>parser
1.  object <span class="apidocSignatureSpan">minty.</span>run
1.  object <span class="apidocSignatureSpan">minty.</span>tools

#### [module minty.createLineRules](#apidoc.module.minty.createLineRules)
1.  [function <span class="apidocSignatureSpan">minty.createLineRules.</span>addLines (type, rule, cluster, lineActivity)](#apidoc.element.minty.createLineRules.addLines)
1.  [function <span class="apidocSignatureSpan">minty.createLineRules.</span>addScopeName (cluster, lineActivity)](#apidoc.element.minty.createLineRules.addScopeName)
1.  [function <span class="apidocSignatureSpan">minty.createLineRules.</span>addVariables (cluster, lineActivity)](#apidoc.element.minty.createLineRules.addVariables)
1.  [function <span class="apidocSignatureSpan">minty.createLineRules.</span>ruler (parsed)](#apidoc.element.minty.createLineRules.ruler)

#### [module minty.parser](#apidoc.module.minty.parser)
1.  [function <span class="apidocSignatureSpan">minty.</span>parser (text)](#apidoc.element.minty.parser.parser)
1.  object <span class="apidocSignatureSpan">minty.parser.</span>parseutils
1.  object <span class="apidocSignatureSpan">minty.parser.</span>types

#### [module minty.run](#apidoc.module.minty.run)
1.  [function <span class="apidocSignatureSpan">minty.run.</span>runFile (fileText, absPath, originalText)](#apidoc.element.minty.run.runFile)
1.  [function <span class="apidocSignatureSpan">minty.run.</span>wrap (wrapText, originalText)](#apidoc.element.minty.run.wrap)

#### [module minty.tools](#apidoc.module.minty.tools)
1.  [function <span class="apidocSignatureSpan">minty.tools.</span>anonFuncCheck (jsText)](#apidoc.element.minty.tools.anonFuncCheck)
1.  [function <span class="apidocSignatureSpan">minty.tools.</span>flattenDeep (array)](#apidoc.element.minty.tools.flattenDeep)



# <a name="apidoc.module.minty"></a>[module minty](#apidoc.module.minty)

#### <a name="apidoc.element.minty.file"></a>[function <span class="apidocSignatureSpan">minty.</span>file (path)](#apidoc.element.minty.file)
- description and source-code
```javascript
function file(path) {
  const JSTEXT = fs.readFileSync(path).toString();
  const parsed = parser(JSTEXT);
  const rules = ruler(parsed);
  const injected = inject(rules, JSTEXT);
  run.runFile(injected, path, JSTEXT);
  return;
}
```
- example usage
```shell
...

Requires Node.js 4.0 or greater.

## How-To

1. 'npm install -g minty' or 'npm install --save-dev minty' (don't use minty in production!)
1. 'const minty = require ('minty');' in the file you'd like to analyze
1. You can execute an entire file by typing 'minty.file(//path to file)'. Note, the file path must be absolute, e.g. 'minty.file
(path.join(__dirname, ../lib/test.js))'
1. You can also 'mintify' a function by typing 'var newFunc = minty.wrap(initialFunc)', and then execute it by calling 'newFunc()'
1. Run your code as usual (e.g. 'node minty.js') to generate the minty output. A new minty folder will appear in your root directory
1. Open the minty.html file in your browser in either the 'file' or 'function' folder (depending on whether you executed a file,
function, or both). Note: data is stored in the mintyVis.js
1. Click forward and back to step through your variables' state as your app executes!

## Gotchas
...
```

#### <a name="apidoc.element.minty.wrap"></a>[function <span class="apidocSignatureSpan">minty.</span>wrap (func)](#apidoc.element.minty.wrap)
- description and source-code
```javascript
function wrap(func) {
  const JSTEXT = func.toString();
  const namedJsFunc = anonFunc(JSTEXT);
  const parsed = parser(namedJsFunc);
  const rules = ruler(parsed);
  const injected = inject(rules, namedJsFunc);
  const mintified = run.wrap(injected, namedJsFunc);
  return function() {
    const args = Array.prototype.slice.call(arguments);
    return mintified.apply(null, args);
  };
}
```
- example usage
```shell
...
Requires Node.js 4.0 or greater.

## How-To

1. 'npm install -g minty' or 'npm install --save-dev minty' (don't use minty in production!)
1. 'const minty = require ('minty');' in the file you'd like to analyze
1. You can execute an entire file by typing 'minty.file(//path to file)'. Note, the file path must be absolute, e.g. 'minty.file
(path.join(__dirname, ../lib/test.js))'
1. You can also 'mintify' a function by typing 'var newFunc = minty.wrap(initialFunc)', and then execute it by calling 'newFunc()'
1. Run your code as usual (e.g. 'node minty.js') to generate the minty output. A new minty folder will appear in your root directory
1. Open the minty.html file in your browser in either the 'file' or 'function' folder (depending on whether you executed a file,
function, or both). Note: data is stored in the mintyVis.js
1. Click forward and back to step through your variables' state as your app executes!

## Gotchas

* If you globally declare a variable without using let, var, or const, we won't track it.
...
```



# <a name="apidoc.module.minty.createLineRules"></a>[module minty.createLineRules](#apidoc.module.minty.createLineRules)

#### <a name="apidoc.element.minty.createLineRules.addLines"></a>[function <span class="apidocSignatureSpan">minty.createLineRules.</span>addLines (type, rule, cluster, lineActivity)](#apidoc.element.minty.createLineRules.addLines)
- description and source-code
```javascript
function addLines(type, rule, cluster, lineActivity) {
  let startLine;
  let endLine;
  cluster.forEach(group => {
    startLine = group.startLine - 1;
    endLine = group.endLine - 1;
    if (!lineActivity[startLine]) lineActivity[startLine] = {};
    if (!lineActivity[startLine].rulesFound) lineActivity[startLine].rulesFound = [];
    if (rule) {
      lineActivity[startLine].rulesFound.push({ action: 'START', rule, type });
    }
    if (!lineActivity[endLine]) lineActivity[endLine] = {};
    if (!lineActivity[endLine].rulesFound) lineActivity[endLine].rulesFound = [];
    if (rule) {
      lineActivity[endLine].rulesFound.push({ action: 'END', rule, type });
    }
  });
}
```
- example usage
```shell
...
function ruler(parsed) {
let lineActivity = {};
Object.keys(parsed).forEach(type => {
  switch (type) {
    case 'BreakStatement':
    case 'ReturnStatement':
    case 'YieldExpression':
      lineRules.addLines(type, 'SWAP', parsed[type], lineActivity);
      break;
    case 'FunctionDeclaration':
    case 'FunctionExpression':
    case 'ArrowFunctionExpression':
    case 'SwitchCase':
      lineRules.addLines(type, 'SCOPE', parsed[type], lineActivity);
      lineRules.addVariables(parsed[type], lineActivity);
...
```

#### <a name="apidoc.element.minty.createLineRules.addScopeName"></a>[function <span class="apidocSignatureSpan">minty.createLineRules.</span>addScopeName (cluster, lineActivity)](#apidoc.element.minty.createLineRules.addScopeName)
- description and source-code
```javascript
function addScopeName(cluster, lineActivity) {

  cluster.forEach(group => {
    const line = lineActivity[group.startLine - 1];
    if (group.name) {
      line.scope = group.name;
    } else if (group.parameters) {
      if (line.variables.variables) {
        line.scope = line.variables.variables.names.join('');
      } else {
        line.scope = 'anonymous function';
      }
    }
  });
}
```
- example usage
```shell
...
  break;
case 'FunctionDeclaration':
case 'FunctionExpression':
case 'ArrowFunctionExpression':
case 'SwitchCase':
  lineRules.addLines(type, 'SCOPE', parsed[type], lineActivity);
  lineRules.addVariables(parsed[type], lineActivity);
  lineRules.addScopeName(parsed[type], lineActivity);
  break;
case 'VariableDeclaration':
  lineRules.addLines(type, null, parsed[type], lineActivity);
  lineRules.addVariables(parsed[type], lineActivity);
  break;
case 'CallExpression':
case 'SwitchStatement':
...
```

#### <a name="apidoc.element.minty.createLineRules.addVariables"></a>[function <span class="apidocSignatureSpan">minty.createLineRules.</span>addVariables (cluster, lineActivity)](#apidoc.element.minty.createLineRules.addVariables)
- description and source-code
```javascript
function addVariables(cluster, lineActivity) {
  cluster.forEach(group => {
    const line = lineActivity[group.startLine - 1];
    if (!line.variables) line.variables = {};
    if (group.parameters) {
      line.variables.parameters = group.parameters;
    }
    if (group.variables) {
      line.variables.variables = {
        names: group.variables,
        kind: group.kind,
      };
    }
  });

}
```
- example usage
```shell
...
  lineRules.addLines(type, 'SWAP', parsed[type], lineActivity);
  break;
case 'FunctionDeclaration':
case 'FunctionExpression':
case 'ArrowFunctionExpression':
case 'SwitchCase':
  lineRules.addLines(type, 'SCOPE', parsed[type], lineActivity);
  lineRules.addVariables(parsed[type], lineActivity);
  lineRules.addScopeName(parsed[type], lineActivity);
  break;
case 'VariableDeclaration':
  lineRules.addLines(type, null, parsed[type], lineActivity);
  lineRules.addVariables(parsed[type], lineActivity);
  break;
case 'CallExpression':
...
```

#### <a name="apidoc.element.minty.createLineRules.ruler"></a>[function <span class="apidocSignatureSpan">minty.createLineRules.</span>ruler (parsed)](#apidoc.element.minty.createLineRules.ruler)
- description and source-code
```javascript
function ruler(parsed) {
  let lineActivity = {};
  Object.keys(parsed).forEach(type => {
    switch (type) {
      case 'BreakStatement':
      case 'ReturnStatement':
      case 'YieldExpression':
        lineRules.addLines(type, 'SWAP', parsed[type], lineActivity);
        break;
      case 'FunctionDeclaration':
      case 'FunctionExpression':
      case 'ArrowFunctionExpression':
      case 'SwitchCase':
        lineRules.addLines(type, 'SCOPE', parsed[type], lineActivity);
        lineRules.addVariables(parsed[type], lineActivity);
        lineRules.addScopeName(parsed[type], lineActivity);
        break;
      case 'VariableDeclaration':
        lineRules.addLines(type, null, parsed[type], lineActivity);
        lineRules.addVariables(parsed[type], lineActivity);
        break;
      case 'CallExpression':
      case 'SwitchStatement':
        lineRules.addLines(type, 'VOID', parsed[type], lineActivity);
        break;
      default:
        lineRules.addLines(type, 'SCOPE', parsed[type], lineActivity);
        break;
    }
  });
  return lineActivity;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.minty.parser"></a>[module minty.parser](#apidoc.module.minty.parser)

#### <a name="apidoc.element.minty.parser.parser"></a>[function <span class="apidocSignatureSpan">minty.</span>parser (text)](#apidoc.element.minty.parser.parser)
- description and source-code
```javascript
function parser(text) {
  parseutils.cache = {};

  ast = esprima.parse(text, {
    loc: true,
  });

  parseutils.asyncTasks.forEach(func => {
    func();
  });
  return parseutils.cache;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.minty.run"></a>[module minty.run](#apidoc.module.minty.run)

#### <a name="apidoc.element.minty.run.runFile"></a>[function <span class="apidocSignatureSpan">minty.run.</span>runFile (fileText, absPath, originalText)](#apidoc.element.minty.run.runFile)
- description and source-code
```javascript
function runFile(fileText, absPath, originalText) {
  const fileJS = fileText.log.join('\n');
  log = [];
  filename = absPath.slice(absPath.lastIndexOf('/') + 1);
  try {
    _eval(fileJS, filename, {
      mintyLog: mintyLog,
    }, true);
  } catch (err) {
    console.log('\n\n#################################################################################\nMinty has found an error
! Please check the out put of ${filename} for more details\n#################################################################################\n');
    errorHandler(err, fileText);
  } finally {
    const output = {
      entry: filename,
      log: log,
    };
    output[filename] = originalText;
    const fileOutput = finalizeOutput(output);
    finalizeRun(fileOutput, 'file');
    console.log('Minty has finished analyzing ${filename}');
  }
}
```
- example usage
```shell
...
**/

function file(path) {
  const JSTEXT = fs.readFileSync(path).toString();
  const parsed = parser(JSTEXT);
  const rules = ruler(parsed);
  const injected = inject(rules, JSTEXT);
  run.runFile(injected, path, JSTEXT);
  return;
}

/**
* turns function to a string, turns function into abstract syntax tree, creates rules to inject monitoring code, and returns function
 that will output HTML file each time it is called
* @param {function}
* @returns {function} each time returned function is executed, an HTML visualization will be created
...
```

#### <a name="apidoc.element.minty.run.wrap"></a>[function <span class="apidocSignatureSpan">minty.run.</span>wrap (wrapText, originalText)](#apidoc.element.minty.run.wrap)
- description and source-code
```javascript
function wrap(wrapText, originalText) {
  let returnStatement;
  log = [];
  filename = wrapText.log[1]
    .split(',')[2]
    .replace(/\s+|\]|\'|\"/g, '');
  const wrapJS = wrapText.log.join('\n');
  return function() {
    const args = Array.prototype.slice.call(arguments);
    try {
      const fn = eval('(${wrapJS})');
      returnStatement = fn.apply(null, args);
    } catch (err) {
      console.log('\n\n#################################################################################\nMinty has found an error
! Please check the out put of ${filename} for more details\n#################################################################################\n');
      errorHandler(err, wrapText);
    } finally {
      const output = {
        entry: filename,
        log: log,
      };
      output[filename] = originalText;
      const wrapOutput = finalizeOutput(output);
      finalizeRun(wrapOutput, 'function');
    }
    return returnStatement;
  };
}
```
- example usage
```shell
...
Requires Node.js 4.0 or greater.

## How-To

1. 'npm install -g minty' or 'npm install --save-dev minty' (don't use minty in production!)
1. 'const minty = require ('minty');' in the file you'd like to analyze
1. You can execute an entire file by typing 'minty.file(//path to file)'. Note, the file path must be absolute, e.g. 'minty.file
(path.join(__dirname, ../lib/test.js))'
1. You can also 'mintify' a function by typing 'var newFunc = minty.wrap(initialFunc)', and then execute it by calling 'newFunc()'
1. Run your code as usual (e.g. 'node minty.js') to generate the minty output. A new minty folder will appear in your root directory
1. Open the minty.html file in your browser in either the 'file' or 'function' folder (depending on whether you executed a file,
function, or both). Note: data is stored in the mintyVis.js
1. Click forward and back to step through your variables' state as your app executes!

## Gotchas

* If you globally declare a variable without using let, var, or const, we won't track it.
...
```



# <a name="apidoc.module.minty.tools"></a>[module minty.tools](#apidoc.module.minty.tools)

#### <a name="apidoc.element.minty.tools.anonFuncCheck"></a>[function <span class="apidocSignatureSpan">minty.tools.</span>anonFuncCheck (jsText)](#apidoc.element.minty.tools.anonFuncCheck)
- description and source-code
```javascript
function anonFuncCheck(jsText) {
  if (jsText[9] === '(') {
    const namedAnonFunc = jsText.replace(jsText[8], ' anonymousFunc');
    return namedAnonFunc;
  }
  return jsText;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.minty.tools.flattenDeep"></a>[function <span class="apidocSignatureSpan">minty.tools.</span>flattenDeep (array)](#apidoc.element.minty.tools.flattenDeep)
- description and source-code
```javascript
function flattenDeep(array) {
  if (array) {
    let flattenArray = [];
    for (let i = 0; i < array.length; i++) {
      const element = array[i];
      if (element.constructor === Array) {
        flattenArray = flattenArray.concat(flattenDeep(element));
      } else {
        flattenArray.push(element);
      }
    }
    return flattenArray;
  }
  return undefined;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
