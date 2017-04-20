# npmdoc-underscore.string

#### api documentation for  [underscore.string (v3.3.4)](http://epeli.github.com/underscore.string/)  [![npm package](https://img.shields.io/npm/v/npmdoc-underscore.string.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-underscore.string) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-underscore.string.svg)](https://travis-ci.org/npmdoc/node-npmdoc-underscore.string)

#### String manipulation extensions for Underscore.js javascript library.

[![NPM](https://nodei.co/npm/underscore.string.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/underscore.string)

- [https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "underscore.string",
    "version": "3.3.4",
    "description": "String manipulation extensions for Underscore.js javascript library.",
    "homepage": "http://epeli.github.com/underscore.string/",
    "contributors": [
        "Esa-Matti Suuronen <esa-matti@suuronen.org> (http://esa-matti.suuronen.org/)",
        "Edward Tsech <edtsech@gmail.com>",
        "Pavel Pravosud <pavel@pravosud.com> (<https://github.com/rwz>)",
        "Sasha Koss <kossnocorp@gmail.com> (http://koss.nocorp.me/)",
        "Vladimir Dronnikov <dronnikov@gmail.com>",
        "Pete Kruckenberg (<https://github.com/kruckenb>)",
        "Paul Chavard <paul@chavard.net> (<http://tchak.net>)",
        "Ed Finkler <coj@funkatron.com> (<http://funkatron.com>)",
        "Christoph Hermann <schtoeffel@gmail.com> (<https://github.com/stoeffel>)"
    ],
    "keywords": [
        "underscore",
        "string"
    ],
    "main": "./index.js",
    "directories": {
        "lib": "./"
    },
    "engines": {
        "node": "*"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/epeli/underscore.string.git"
    },
    "bugs": {
        "url": "https://github.com/epeli/underscore.string/issues"
    },
    "license": "MIT",
    "scripts": {
        "test": "npm run test:lint && npm run test:unit && npm run coverage",
        "test:unit": "mocha --ui=qunit tests",
        "test:lint": "eslint -c .eslintrc .",
        "coverage": "istanbul cover ./node_modules/mocha/bin/_mocha  -- --report=lcov --ui=qunit tests",
        "build": "npm run build:clean && npm run build:bundle && npm run build:min",
        "build:clean": "rm -rf dist",
        "build:bundle": "mkdir dist && browserify index.js -o dist/underscore.string.js -p browserify-header -s s",
        "build:min": "uglifyjs dist/underscore.string.js -o dist/underscore.string.min.js --comments",
        "release": "npm test && npm run release:version && npm run build && npm run release:push",
        "release:version": "node scripts/bump-version.js",
        "release:push": "node scripts/push-tags.js"
    },
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
    "jshintConfig": {
        "node": true,
        "browser": true,
        "qunit": true,
        "globals": {
            "s": true
        }
    },
    "dependencies": {
        "sprintf-js": "^1.0.3",
        "util-deprecate": "^1.0.2"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
