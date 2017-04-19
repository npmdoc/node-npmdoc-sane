# npmdoc-sane

#### api documentation for  [sane (v1.6.0)](https://github.com/amasad/sane)  [![npm package](https://img.shields.io/npm/v/npmdoc-sane.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sane) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sane.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sane)

#### Sane aims to be fast, small, and reliable file system watcher.

[![NPM](https://nodei.co/npm/sane.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/sane)

- [https://npmdoc.github.io/node-npmdoc-sane/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-sane/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sane/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sane/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-sane/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-sane/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "amasad"
    },
    "bin": {
        "sane": "./src/cli.js"
    },
    "bugs": {
        "url": "https://github.com/amasad/sane/issues"
    },
    "dependencies": {
        "anymatch": "^1.3.0",
        "exec-sh": "^0.2.0",
        "fb-watchman": "^1.8.0",
        "minimatch": "^3.0.2",
        "minimist": "^1.1.1",
        "walker": "~1.0.5",
        "watch": "~0.10.0"
    },
    "description": "Sane aims to be fast, small, and reliable file system watcher.",
    "devDependencies": {
        "jshint": "^2.5.10",
        "mocha": "~1.17.1",
        "rimraf": "~2.2.6",
        "tmp": "0.0.27"
    },
    "directories": {},
    "dist": {
        "shasum": "9610c452307a135d29c1fdfe2547034180c46775",
        "tarball": "https://registry.npmjs.org/sane/-/sane-1.6.0.tgz"
    },
    "engines": {
        "node": ">=0.6.0"
    },
    "files": [
        "src",
        "index.js"
    ],
    "gitHead": "b9c60d9dd3c5a81f50ef0f05828038191fdfa68b",
    "homepage": "https://github.com/amasad/sane",
    "keywords": [
        "watch",
        "file",
        "fswatcher",
        "watchfile",
        "fs",
        "watching"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "amasad"
        },
        {
            "name": "stefanpenner"
        }
    ],
    "name": "sane",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/amasad/sane.git"
    },
    "scripts": {
        "prepublish": "jshint --config=.jshintrc src/ index.js && mocha --bail",
        "test": "jshint --config=.jshintrc src/ index.js && mocha --bail test/test.js && mocha --bail test/utils-test.js",
        "test:debug": "mocha debug --bail"
    },
    "version": "1.6.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
