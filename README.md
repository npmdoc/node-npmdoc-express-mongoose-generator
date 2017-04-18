# npmdoc-express-mongoose-generator

#### api documentation for  [express-mongoose-generator (v3.0.2)](https://github.com/DamienP33/express-mongoose-generator#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-express-mongoose-generator.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-express-mongoose-generator) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-express-mongoose-generator.svg)](https://travis-ci.org/npmdoc/node-npmdoc-express-mongoose-generator)

#### It’s a mongoose model, REST controller and Express router code generator for Express.js 4 application

[![NPM](https://nodei.co/npm/express-mongoose-generator.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/express-mongoose-generator)

- [https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Damien Perrier"
    },
    "bin": {
        "mongoose-gen": "./bin/mongoose-gen"
    },
    "bugs": {
        "url": "https://github.com/DamienP33/express-mongoose-generator/issues"
    },
    "contributors": [
        {
            "name": "romuloctba"
        }
    ],
    "dependencies": {
        "async": "^0.9.0",
        "commander": "^2.5.0"
    },
    "description": "It’s a mongoose model, REST controller and Express router code generator for Express.js 4 application",
    "devDependencies": {
        "jscs": "^2.5.1",
        "jshint": "^2.8.0",
        "mkdirp": "^0.5.0",
        "mocha": "^2.0.1",
        "nexpect": "^0.4.2",
        "rimraf": "^2.2.8"
    },
    "directories": {},
    "dist": {
        "shasum": "32ec12857a1adadcf55fe2da081d2b4d49120c8e",
        "tarball": "https://registry.npmjs.org/express-mongoose-generator/-/express-mongoose-generator-3.0.2.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "files": [
        "LICENSE",
        "bin/",
        "templates/",
        "lib/"
    ],
    "gitHead": "ef3918d5414e27377fbf5203d42c9045d7be5735",
    "homepage": "https://github.com/DamienP33/express-mongoose-generator#readme",
    "keywords": [
        "mongodb",
        "mongoose",
        "express",
        "generator",
        "rest",
        "restfull",
        "api",
        "app",
        "web"
    ],
    "license": "MIT",
    "main": "bin/mongoose-gen",
    "maintainers": [
        {
            "name": "damienp33"
        }
    ],
    "name": "express-mongoose-generator",
    "optionalDependencies": {},
    "preferGlobal": true,
    "repository": {
        "type": "git",
        "url": "git+https://github.com/DamienP33/express-mongoose-generator.git"
    },
    "scripts": {
        "cs": "jscs ./**/*.js ./bin/mongoose-gen",
        "lint": "jshint ./**/*.js ./bin/mongoose-gen",
        "test": "mocha --reporter spec --bail --check-leaks test/"
    },
    "version": "3.0.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
