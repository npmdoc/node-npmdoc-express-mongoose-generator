# api documentation for  [express-mongoose-generator (v3.0.2)](https://github.com/DamienP33/express-mongoose-generator#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-express-mongoose-generator.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-express-mongoose-generator) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-express-mongoose-generator.svg)](https://travis-ci.org/npmdoc/node-npmdoc-express-mongoose-generator)
#### It’s a mongoose model, REST controller and Express router code generator for Express.js 4 application

[![NPM](https://nodei.co/npm/express-mongoose-generator.png?downloads=true)](https://www.npmjs.com/package/express-mongoose-generator)

[![apidoc](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-express-mongoose-generator_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-express-mongoose-generator/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Damien Perrier",
        "email": "damienperrier33@gmail.com"
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
            "name": "damienp33",
            "email": "damienperrier33@gmail.com"
        }
    ],
    "name": "express-mongoose-generator",
    "optionalDependencies": {},
    "preferGlobal": true,
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module express-mongoose-generator](#apidoc.module.express-mongoose-generator)
1.  object <span class="apidocSignatureSpan">express-mongoose-generator.</span>fileTools
1.  object <span class="apidocSignatureSpan">express-mongoose-generator.</span>formatTools
1.  object <span class="apidocSignatureSpan">express-mongoose-generator.</span>generators

#### [module express-mongoose-generator.fileTools](#apidoc.module.express-mongoose-generator.fileTools)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>createDirIfIsNotDefined (dirPath, dirName, cb)](#apidoc.element.express-mongoose-generator.fileTools.createDirIfIsNotDefined)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>loadTemplateSync (name)](#apidoc.element.express-mongoose-generator.fileTools.loadTemplateSync)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>writeFile (path, contents, mode, cb)](#apidoc.element.express-mongoose-generator.fileTools.writeFile)

#### [module express-mongoose-generator.formatTools](#apidoc.module.express-mongoose-generator.formatTools)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.formatTools.</span>getFieldsForModelTemplate (fields)](#apidoc.element.express-mongoose-generator.formatTools.getFieldsForModelTemplate)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.formatTools.</span>pluralize (word)](#apidoc.element.express-mongoose-generator.formatTools.pluralize)

#### [module express-mongoose-generator.generators](#apidoc.module.express-mongoose-generator.generators)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateController (path, modelName, modelFields, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateController)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateModel (path, modelName, modelFields, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateModel)
1.  [function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateRouter (path, modelName, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateRouter)



# <a name="apidoc.module.express-mongoose-generator"></a>[module express-mongoose-generator](#apidoc.module.express-mongoose-generator)



# <a name="apidoc.module.express-mongoose-generator.fileTools"></a>[module express-mongoose-generator.fileTools](#apidoc.module.express-mongoose-generator.fileTools)

#### <a name="apidoc.element.express-mongoose-generator.fileTools.createDirIfIsNotDefined"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>createDirIfIsNotDefined (dirPath, dirName, cb)](#apidoc.element.express-mongoose-generator.fileTools.createDirIfIsNotDefined)
- description and source-code
```javascript
function createDirIfIsNotDefined(dirPath, dirName, cb) {
    if (!fs.existsSync(dirPath + '/' + dirName)){
        fs.mkdirSync(dirPath + '/' + dirName);
        console.info(cliStyles.cyan + '\tcreate' + cliStyles.reset + ': ' + dirPath + '/' + dirName);
    }

    cb();
}
```
- example usage
```shell
...

var model = ft.loadTemplateSync('model.js');
model = model.replace(/{modelName}/, modelName);
model = model.replace(/{schemaName}/g, schemaName);
model = model.replace(/{fields}/, fields);

if (generateMethod == 't') {
    ft.createDirIfIsNotDefined(path, 'models', function () {
        ft.writeFile(path + '/models/' + modelName + 'Model.js', model, null, cb);
    });
} else {
    ft.createDirIfIsNotDefined(path, modelName, function () {
        ft.writeFile(path + '/' + modelName + '/' + modelName + 'Model.js', model, null, cb);
    });
}
...
```

#### <a name="apidoc.element.express-mongoose-generator.fileTools.loadTemplateSync"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>loadTemplateSync (name)](#apidoc.element.express-mongoose-generator.fileTools.loadTemplateSync)
- description and source-code
```javascript
function loadTemplateSync(name) {
    return fs.readFileSync(path.join(__dirname, '..', 'templates', name), 'utf-8');
}
```
- example usage
```shell
...
 * @param {string} generateMethod
 * @param {function} cb
 */
function generateModel(path, modelName, modelFields, generateMethod, cb) {
var fields = formatTools.getFieldsForModelTemplate(modelFields);
var schemaName = modelName + 'Schema';

var model = ft.loadTemplateSync('model.js');
model = model.replace(/{modelName}/, modelName);
model = model.replace(/{schemaName}/g, schemaName);
model = model.replace(/{fields}/, fields);

if (generateMethod == 't') {
    ft.createDirIfIsNotDefined(path, 'models', function () {
        ft.writeFile(path + '/models/' + modelName + 'Model.js', model, null, cb);
...
```

#### <a name="apidoc.element.express-mongoose-generator.fileTools.writeFile"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.fileTools.</span>writeFile (path, contents, mode, cb)](#apidoc.element.express-mongoose-generator.fileTools.writeFile)
- description and source-code
```javascript
function writeFile(path, contents, mode, cb) {
    fs.writeFile(path, contents, {mode: mode || 0666}, function (err) {
        if (err) { throw err; }
        console.info(cliStyles.cyan + '\tcreate' + cliStyles.reset + ': ' + path);
        cb();
    });
}
```
- example usage
```shell
...
 * Write a file
 * @param {string} path file path to write
 * @param {string} contents file contents to write
 * @param {int} mode write mode
 * @param {function} cb callback
 */
function writeFile(path, contents, mode, cb) {
    fs.writeFile(path, contents, {mode: mode || 0666}, function (err) {
        if (err) { throw err; }
        console.info(cliStyles.cyan + '\tcreate' + cliStyles.reset + ': ' + path);
        cb();
    });
}

/**
...
```



# <a name="apidoc.module.express-mongoose-generator.formatTools"></a>[module express-mongoose-generator.formatTools](#apidoc.module.express-mongoose-generator.formatTools)

#### <a name="apidoc.element.express-mongoose-generator.formatTools.getFieldsForModelTemplate"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.formatTools.</span>getFieldsForModelTemplate (fields)](#apidoc.element.express-mongoose-generator.formatTools.getFieldsForModelTemplate)
- description and source-code
```javascript
function getFieldsForModelTemplate(fields) {
    var lg = fields.length - 1;

    var modelFields = '{\r';
    fields.forEach(function(field, index, array) {
        modelFields += '\t\'' + field.name + '\' : ' + (allowedFieldsTypes[field.type]).name;
        modelFields += (lg > index) ? ',\r' : '\r';
        if (field.reference) {
            modelFields = modelFields.replace(/{ref}/, field.reference);
        }
    });
    modelFields += '}';

    return modelFields;
}
```
- example usage
```shell
...
 * @param {string} path
 * @param {string} modelName
 * @param {array} modelFields
 * @param {string} generateMethod
 * @param {function} cb
 */
function generateModel(path, modelName, modelFields, generateMethod, cb) {
var fields = formatTools.getFieldsForModelTemplate(modelFields);
var schemaName = modelName + 'Schema';

var model = ft.loadTemplateSync('model.js');
model = model.replace(/{modelName}/, modelName);
model = model.replace(/{schemaName}/g, schemaName);
model = model.replace(/{fields}/, fields);
...
```

#### <a name="apidoc.element.express-mongoose-generator.formatTools.pluralize"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.formatTools.</span>pluralize (word)](#apidoc.element.express-mongoose-generator.formatTools.pluralize)
- description and source-code
```javascript
function pluralize(word) {
    return word + 's';
}
```
- example usage
```shell
...

    createFields += '\t\t\t' + field + ' : req.body.' + field;
    createFields += ((fields.length - 1) > index) ? ',\r' : '\r';
});

controller = controller.replace(/{modelName}/g, modelName + 'Model');
controller = controller.replace(/{name}/g, modelName);
controller = controller.replace(/{pluralName}/g, formatTools.pluralize(modelName));
controller = controller.replace(/{controllerName}/g, modelName + 'Controller');
controller = controller.replace(/{createFields}/g, createFields);
controller = controller.replace(/{updateFields}/g, updateFields);

if (generateMethod == 't') {
    ft.createDirIfIsNotDefined(path, 'controllers', function () {
        controller = controller.replace(/{modelPath}/g, '\'../models/' + modelName + 'Model.js\'');
...
```



# <a name="apidoc.module.express-mongoose-generator.generators"></a>[module express-mongoose-generator.generators](#apidoc.module.express-mongoose-generator.generators)

#### <a name="apidoc.element.express-mongoose-generator.generators.generateController"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateController (path, modelName, modelFields, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateController)
- description and source-code
```javascript
function generateController(path, modelName, modelFields, generateMethod, cb) {
    var controller = ft.loadTemplateSync('controller.js');

    var updateFields = '';
    var createFields = '\r';

    modelFields.forEach(function (f, index, fields) {
        var field = f.name;

        updateFields += modelName + '.' + field + ' = req.body.' + field + ' ? req.body.' + field + ' : ' +
            modelName + '.' + field + ';';
        updateFields += '\r\t\t\t';

        createFields += '\t\t\t' + field + ' : req.body.' + field;
        createFields += ((fields.length - 1) > index) ? ',\r' : '\r';
    });

    controller = controller.replace(/{modelName}/g, modelName + 'Model');
    controller = controller.replace(/{name}/g, modelName);
    controller = controller.replace(/{pluralName}/g, formatTools.pluralize(modelName));
    controller = controller.replace(/{controllerName}/g, modelName + 'Controller');
    controller = controller.replace(/{createFields}/g, createFields);
    controller = controller.replace(/{updateFields}/g, updateFields);

    if (generateMethod == 't') {
        ft.createDirIfIsNotDefined(path, 'controllers', function () {
            controller = controller.replace(/{modelPath}/g, '\'../models/' + modelName + 'Model.js\'');
            ft.writeFile(path + '/controllers/' + modelName + 'Controller.js', controller, null, cb);
        });
    } else {
        ft.createDirIfIsNotDefined(path, modelName, function () {
            controller = controller.replace(/{modelPath}/g, '\'./' + modelName + 'Model.js\'');
            ft.writeFile(path + '/' + modelName + '/' + modelName + 'Controller.js', controller, null, cb);
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-mongoose-generator.generators.generateModel"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateModel (path, modelName, modelFields, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateModel)
- description and source-code
```javascript
function generateModel(path, modelName, modelFields, generateMethod, cb) {
    var fields = formatTools.getFieldsForModelTemplate(modelFields);
    var schemaName = modelName + 'Schema';

    var model = ft.loadTemplateSync('model.js');
    model = model.replace(/{modelName}/, modelName);
    model = model.replace(/{schemaName}/g, schemaName);
    model = model.replace(/{fields}/, fields);

    if (generateMethod == 't') {
        ft.createDirIfIsNotDefined(path, 'models', function () {
            ft.writeFile(path + '/models/' + modelName + 'Model.js', model, null, cb);
        });
    } else {
        ft.createDirIfIsNotDefined(path, modelName, function () {
            ft.writeFile(path + '/' + modelName + '/' + modelName + 'Model.js', model, null, cb);
        });
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.express-mongoose-generator.generators.generateRouter"></a>[function <span class="apidocSignatureSpan">express-mongoose-generator.generators.</span>generateRouter (path, modelName, generateMethod, cb)](#apidoc.element.express-mongoose-generator.generators.generateRouter)
- description and source-code
```javascript
function generateRouter(path, modelName, generateMethod, cb) {
    var router = ft.loadTemplateSync('router.js');
    router = router.replace(/{controllerName}/g, modelName + 'Controller');

    if (generateMethod == 't') {
        ft.createDirIfIsNotDefined(path, 'routes', function () {
            router = router.replace(/{controllerPath}/g, '\'../controllers/' + modelName + 'Controller.js\'');
            ft.writeFile(path + '/routes/' + modelName + 'Routes.js', router, null, cb);
        });
    } else {
        ft.createDirIfIsNotDefined(path, modelName, function () {
            router = router.replace(/{controllerPath}/g, '\'./' + modelName + 'Controller.js\'');
            ft.writeFile(path + '/' + modelName + '/' + modelName + 'Routes.js', router, null, cb);
        });
    }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
