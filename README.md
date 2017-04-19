# npmdoc-minty

#### api documentation for  [minty (v0.5.10)](https://www.mintyjs.com)  [![npm package](https://img.shields.io/npm/v/npmdoc-minty.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-minty) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-minty.svg)](https://travis-ci.org/npmdoc/node-npmdoc-minty)

#### Node process visualization

[![NPM](https://nodei.co/npm/minty.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/minty)

- [https://npmdoc.github.io/node-npmdoc-minty/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-minty/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-minty/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-minty/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ted Zilist"
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
            "name": "angieyeh"
        },
        {
            "name": "kaizendad"
        },
        {
            "name": "tzilist"
        }
    ],
    "name": "minty",
    "optionalDependencies": {},
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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
