# npmdoc-underscore.string

#### basic api documentation for  [underscore.string (v3.3.4)](http://epeli.github.com/underscore.string/)  [![npm package](https://img.shields.io/npm/v/npmdoc-underscore.string.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-underscore.string) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-underscore.string.svg)](https://travis-ci.org/npmdoc/node-npmdoc-underscore.string)

#### String manipulation extensions for Underscore.js javascript library.

[![NPM](https://nodei.co/npm/underscore.string.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/underscore.string)

- [https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/epeli/underscore.string/issues"
    },
    "contributors": [
        {
            "name": "Esa-Matti Suuronen",
            "url": "http://esa-matti.suuronen.org/"
        },
        {
            "name": "Edward Tsech"
        },
        {
            "name": "Pavel Pravosud",
            "url": "<https://github.com/rwz>"
        },
        {
            "name": "Sasha Koss",
            "url": "http://koss.nocorp.me/"
        },
        {
            "name": "Vladimir Dronnikov"
        },
        {
            "name": "Pete Kruckenberg",
            "url": "<https://github.com/kruckenb>"
        },
        {
            "name": "Paul Chavard",
            "url": "<http://tchak.net>"
        },
        {
            "name": "Ed Finkler",
            "url": "<http://funkatron.com>"
        },
        {
            "name": "Christoph Hermann",
            "url": "<https://github.com/stoeffel>"
        }
    ],
    "dependencies": {
        "sprintf-js": "^1.0.3",
        "util-deprecate": "^1.0.2"
    },
    "description": "String manipulation extensions for Underscore.js javascript library.",
    "devDependencies": {
        "browserify": "^13.0.0",
        "browserify-header": "^0.9.2",
        "eslint": "^1.10.3",
        "istanbul": "^0.4.2",
        "mocha": "^2.1.0",
        "mocha-lcov-reporter": "^1.0.0",
        "replace": "^0.3.0",
        "uglifyjs": "^2.4.10",
        "underscore": "^1.7.0"
    },
    "directories": {
        "lib": "./"
    },
    "dist": {
        "shasum": "2c2a3f9f83e64762fdc45e6ceac65142864213db",
        "tarball": "https://registry.npmjs.org/underscore.string/-/underscore.string-3.3.4.tgz"
    },
    "engines": {
        "node": "*"
    },
    "gitHead": "2f78f0d6e36d553484a1bf5fe5ed1998f013dea5",
    "homepage": "http://epeli.github.com/underscore.string/",
    "jshintConfig": {
        "node": true,
        "browser": true,
        "qunit": true,
        "globals": {
            "s": true
        }
    },
    "keywords": [
        "underscore",
        "string"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "edtsech"
        },
        {
            "name": "rwz"
        },
        {
            "name": "epeli"
        },
        {
            "name": "schtoeffel"
        }
    ],
    "name": "underscore.string",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/epeli/underscore.string.git"
    },
    "scripts": {
        "build": "npm run build:clean && npm run build:bundle && npm run build:min",
        "build:bundle": "mkdir dist && browserify index.js -o dist/underscore.string.js -p browserify-header -s s",
        "build:clean": "rm -rf dist",
        "build:min": "uglifyjs dist/underscore.string.js -o dist/underscore.string.min.js --comments",
        "coverage": "istanbul cover ./node_modules/mocha/bin/_mocha  -- --report=lcov --ui=qunit tests",
        "release": "npm test && npm run release:version && npm run build && npm run release:push",
        "release:push": "node scripts/push-tags.js",
        "release:version": "node scripts/bump-version.js",
        "test": "npm run test:lint && npm run test:unit && npm run coverage",
        "test:lint": "eslint -c .eslintrc .",
        "test:unit": "mocha --ui=qunit tests"
    },
    "version": "3.3.4",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
