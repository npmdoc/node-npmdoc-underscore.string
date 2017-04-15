# api documentation for  [underscore.string (v3.3.4)](http://epeli.github.com/underscore.string/)  [![npm package](https://img.shields.io/npm/v/npmdoc-underscore.string.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-underscore.string) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-underscore.string.svg)](https://travis-ci.org/npmdoc/node-npmdoc-underscore.string)
#### String manipulation extensions for Underscore.js javascript library.

[![NPM](https://nodei.co/npm/underscore.string.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/underscore.string)

[![apidoc](https://npmdoc.github.io/node-npmdoc-underscore.string/build/screenCapture.buildCi.browser.apidoc.html.png)](https://npmdoc.github.io/node-npmdoc-underscore.string/build/apidoc.html)

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
    "version": "3.3.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module underscore.string](#apidoc.module.underscore.string)
1.  [function <span class="apidocSignatureSpan">underscore.</span>string (value)](#apidoc.element.underscore.string.string)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>camelcase (str, decapitalize)](#apidoc.element.underscore.string.camelcase)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>camelize (str, decapitalize)](#apidoc.element.underscore.string.camelize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>capitalize (str, lowercaseRest)](#apidoc.element.underscore.string.capitalize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>center (str, length, padStr)](#apidoc.element.underscore.string.center)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>chars (str)](#apidoc.element.underscore.string.chars)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>chop (str, step)](#apidoc.element.underscore.string.chop)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>classify (str)](#apidoc.element.underscore.string.classify)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>clean (str)](#apidoc.element.underscore.string.clean)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>cleanDiacritics (str)](#apidoc.element.underscore.string.cleanDiacritics)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>contains (str, needle)](#apidoc.element.underscore.string.contains)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>count (str, substr)](#apidoc.element.underscore.string.count)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>dasherize (str)](#apidoc.element.underscore.string.dasherize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>decapitalize (str)](#apidoc.element.underscore.string.decapitalize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>dedent (str, pattern)](#apidoc.element.underscore.string.dedent)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>endsWith (str, ends, position)](#apidoc.element.underscore.string.endsWith)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>escapeHTML (str)](#apidoc.element.underscore.string.escapeHTML)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>escapeRegExp (str)](#apidoc.element.underscore.string.escapeRegExp)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>exports ()](#apidoc.element.underscore.string.exports)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>humanize (str)](#apidoc.element.underscore.string.humanize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>include (str, needle)](#apidoc.element.underscore.string.include)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>insert (str, i, substr)](#apidoc.element.underscore.string.insert)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>isBlank (str)](#apidoc.element.underscore.string.isBlank)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>join ()](#apidoc.element.underscore.string.join)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>levenshtein (str1, str2)](#apidoc.element.underscore.string.levenshtein)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>lines (str)](#apidoc.element.underscore.string.lines)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>ljust (str, length, padStr)](#apidoc.element.underscore.string.ljust)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>lpad (str, length, padStr)](#apidoc.element.underscore.string.lpad)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>lrpad (str, length, padStr)](#apidoc.element.underscore.string.lrpad)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>lstrip (str, characters)](#apidoc.element.underscore.string.lstrip)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>ltrim (str, characters)](#apidoc.element.underscore.string.ltrim)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>map (str, callback)](#apidoc.element.underscore.string.map)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>mapChars (str, callback)](#apidoc.element.underscore.string.mapChars)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>naturalCmp (str1, str2)](#apidoc.element.underscore.string.naturalCmp)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>numberFormat (number, dec, dsep, tsep)](#apidoc.element.underscore.string.numberFormat)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>pad (str, length, padStr, type)](#apidoc.element.underscore.string.pad)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>pred (str)](#apidoc.element.underscore.string.pred)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>prune (str, length, pruneStr)](#apidoc.element.underscore.string.prune)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>q (str, quoteChar)](#apidoc.element.underscore.string.q)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>quote (str, quoteChar)](#apidoc.element.underscore.string.quote)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>repeat (str, qty, separator)](#apidoc.element.underscore.string.repeat)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>replaceAll (str, find, replace, ignorecase)](#apidoc.element.underscore.string.replaceAll)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>reverse (str)](#apidoc.element.underscore.string.reverse)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>rjust (str, length, padStr)](#apidoc.element.underscore.string.rjust)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>rpad (str, length, padStr)](#apidoc.element.underscore.string.rpad)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>rstrip (str, characters)](#apidoc.element.underscore.string.rstrip)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>rtrim (str, characters)](#apidoc.element.underscore.string.rtrim)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>slugify (str)](#apidoc.element.underscore.string.slugify)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>splice (str, i, howmany, substr)](#apidoc.element.underscore.string.splice)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>sprintf ()](#apidoc.element.underscore.string.sprintf)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>startsWith (str, starts, position)](#apidoc.element.underscore.string.startsWith)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>strLeft (str, sep)](#apidoc.element.underscore.string.strLeft)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>strLeftBack (str, sep)](#apidoc.element.underscore.string.strLeftBack)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>strRight (str, sep)](#apidoc.element.underscore.string.strRight)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>strRightBack (str, sep)](#apidoc.element.underscore.string.strRightBack)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>strip (str, characters)](#apidoc.element.underscore.string.strip)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>stripTags (str)](#apidoc.element.underscore.string.stripTags)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>succ (str)](#apidoc.element.underscore.string.succ)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>surround (str, wrapper)](#apidoc.element.underscore.string.surround)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>swapCase (str)](#apidoc.element.underscore.string.swapCase)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>titleize (str)](#apidoc.element.underscore.string.titleize)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toBool (str, trueValues, falseValues)](#apidoc.element.underscore.string.toBool)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toBoolean (str, trueValues, falseValues)](#apidoc.element.underscore.string.toBoolean)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toNumber (num, precision)](#apidoc.element.underscore.string.toNumber)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toSentence (array, separator, lastSeparator, serial)](#apidoc.element.underscore.string.toSentence)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toSentenceSerial (array, sep, lastSep)](#apidoc.element.underscore.string.toSentenceSerial)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>toString ()](#apidoc.element.underscore.string.toString)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>trim (str, characters)](#apidoc.element.underscore.string.trim)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>truncate (str, length, truncateStr)](#apidoc.element.underscore.string.truncate)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>underscored (str)](#apidoc.element.underscore.string.underscored)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>unescapeHTML (str)](#apidoc.element.underscore.string.unescapeHTML)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>unquote (str, quoteChar)](#apidoc.element.underscore.string.unquote)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>vsprintf ()](#apidoc.element.underscore.string.vsprintf)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>words (str, delimiter)](#apidoc.element.underscore.string.words)
1.  [function <span class="apidocSignatureSpan">underscore.string.</span>wrap (str, options)](#apidoc.element.underscore.string.wrap)
1.  string <span class="apidocSignatureSpan">underscore.string.</span>VERSION



# <a name="apidoc.module.underscore.string"></a>[module underscore.string](#apidoc.module.underscore.string)

#### <a name="apidoc.element.underscore.string.string"></a>[function <span class="apidocSignatureSpan">underscore.</span>string (value)](#apidoc.element.underscore.string.string)
- description and source-code
```javascript
function s(value) {
<span class="apidocCodeCommentSpan">  /* jshint validthis: true */
</span>  if (!(this instanceof s)) return new s(value);
  this._wrapped = value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.camelcase"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>camelcase (str, decapitalize)](#apidoc.element.underscore.string.camelcase)
- description and source-code
```javascript
function camelize(str, decapitalize) {
  str = trim(str).replace(/[-_\s]+(.)?/g, function(match, c) {
    return c ? c.toUpperCase() : '';
  });

  if (decapitalize === true) {
    return decap(str);
  } else {
    return str;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.camelize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>camelize (str, decapitalize)](#apidoc.element.underscore.string.camelize)
- description and source-code
```javascript
function camelize(str, decapitalize) {
  str = trim(str).replace(/[-_\s]+(.)?/g, function(match, c) {
    return c ? c.toUpperCase() : '';
  });

  if (decapitalize === true) {
    return decap(str);
  } else {
    return str;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.capitalize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>capitalize (str, lowercaseRest)](#apidoc.element.underscore.string.capitalize)
- description and source-code
```javascript
function capitalize(str, lowercaseRest) {
  str = makeString(str);
  var remainingChars = !lowercaseRest ? str.slice(1) : str.slice(1).toLowerCase();

  return str.charAt(0).toUpperCase() + remainingChars;
}
```
- example usage
```shell
...
'''

or load the full library to enable chaining

'''javascript
var s = require("underscore.string");

s("   epeli  ").trim().capitalize().value();
// => "Epeli"
'''

but especially when using with [Browserify][] the individual function approach
is recommended because using it you only add those functions to your bundle you
use.
...
```

#### <a name="apidoc.element.underscore.string.center"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>center (str, length, padStr)](#apidoc.element.underscore.string.center)
- description and source-code
```javascript
function lrpad(str, length, padStr) {
  return pad(str, length, padStr, 'both');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.chars"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>chars (str)](#apidoc.element.underscore.string.chars)
- description and source-code
```javascript
function chars(str) {
  return makeString(str).split('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.chop"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>chop (str, step)](#apidoc.element.underscore.string.chop)
- description and source-code
```javascript
function chop(str, step) {
  if (str == null) return [];
  str = String(str);
  step = ~~step;
  return step > 0 ? str.match(new RegExp('.{1,' + step + '}', 'g')) : [str];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.classify"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>classify (str)](#apidoc.element.underscore.string.classify)
- description and source-code
```javascript
function classify(str) {
  str = makeString(str);
  return capitalize(camelize(str.replace(/[\W_]/g, ' ')).replace(/\s/g, ''));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.clean"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>clean (str)](#apidoc.element.underscore.string.clean)
- description and source-code
```javascript
function clean(str) {
  return trim(str).replace(/\s\s+/g, ' ');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.cleanDiacritics"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>cleanDiacritics (str)](#apidoc.element.underscore.string.cleanDiacritics)
- description and source-code
```javascript
function cleanDiacritics(str) {
  return makeString(str).replace(/.{1}/g, function(c){
    var index = from.indexOf(c);
    return index === -1 ? c : to[index];
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.contains"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>contains (str, needle)](#apidoc.element.underscore.string.contains)
- description and source-code
```javascript
function include(str, needle) {
  if (needle === '') return true;
  return makeString(str).indexOf(needle) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.count"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>count (str, substr)](#apidoc.element.underscore.string.count)
- description and source-code
```javascript
count = function (str, substr) {
  str = makeString(str);
  substr = makeString(substr);

  if (str.length === 0 || substr.length === 0) return 0;

  return str.split(substr).length - 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.dasherize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>dasherize (str)](#apidoc.element.underscore.string.dasherize)
- description and source-code
```javascript
function dasherize(str) {
  return trim(str).replace(/([A-Z])/g, '-$1').replace(/[-_\s]+/g, '-').toLowerCase();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.decapitalize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>decapitalize (str)](#apidoc.element.underscore.string.decapitalize)
- description and source-code
```javascript
function decapitalize(str) {
  str = makeString(str);
  return str.charAt(0).toLowerCase() + str.slice(1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.dedent"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>dedent (str, pattern)](#apidoc.element.underscore.string.dedent)
- description and source-code
```javascript
function dedent(str, pattern) {
  str = makeString(str);
  var indent = getIndent(str);
  var reg;

  if (indent === 0) return str;

  if (typeof pattern === 'string') {
    reg = new RegExp('^' + pattern, 'gm');
  } else {
    reg = new RegExp('^[ \\t]{' + indent + '}', 'gm');
  }

  return str.replace(reg, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.endsWith"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>endsWith (str, ends, position)](#apidoc.element.underscore.string.endsWith)
- description and source-code
```javascript
function endsWith(str, ends, position) {
  str = makeString(str);
  ends = '' + ends;
  if (typeof position == 'undefined') {
    position = str.length - ends.length;
  } else {
    position = Math.min(toPositive(position), str.length) - ends.length;
  }
  return position >= 0 && str.indexOf(ends, position) === position;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.escapeHTML"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>escapeHTML (str)](#apidoc.element.underscore.string.escapeHTML)
- description and source-code
```javascript
function escapeHTML(str) {

  return makeString(str).replace(regex, function(m) {
    return '&' + escapeChars[m] + ';';
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.escapeRegExp"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>escapeRegExp (str)](#apidoc.element.underscore.string.escapeRegExp)
- description and source-code
```javascript
function escapeRegExp(str) {
  return makeString(str).replace(/([.*+?^=!:${}()|[\]\/\\])/g, '\\$1');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.exports"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>exports ()](#apidoc.element.underscore.string.exports)
- description and source-code
```javascript
exports = function () {
  var result = {};

  for (var prop in this) {
    if (!this.hasOwnProperty(prop) || prop.match(/^(?:include|contains|reverse|join|map|wrap)$/)) continue;
    result[prop] = this[prop];
  }

  return result;
}
```
- example usage
```shell
...
[RequireJS]: http://requirejs.org/

### Underscore.js/Lo-Dash integration

It is still possible use as Underscore.js/Lo-Dash extension

'''javascript
_.mixin(s.exports());
'''
But it's not recommended since 'include', 'contains', 'reverse' and 'join'
are dropped because they collide with the functions already defined by Underscore.js.

### Lo-Dash-FP/Ramda integration

If you want to use underscore.string with [ramdajs](http://ramdajs.com/) or [Lo-Dash-FP](https://github.com/lodash/lodash-fp) you
 can use [underscore.string.fp](https://github.com/stoeffel/underscore.string.fp).
...
```

#### <a name="apidoc.element.underscore.string.humanize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>humanize (str)](#apidoc.element.underscore.string.humanize)
- description and source-code
```javascript
function humanize(str) {
  return capitalize(trim(underscored(str).replace(/_id$/, '').replace(/_/g, ' ')));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.include"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>include (str, needle)](#apidoc.element.underscore.string.include)
- description and source-code
```javascript
function include(str, needle) {
  if (needle === '') return true;
  return makeString(str).indexOf(needle) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.insert"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>insert (str, i, substr)](#apidoc.element.underscore.string.insert)
- description and source-code
```javascript
function insert(str, i, substr) {
  return splice(str, i, 0, substr);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.isBlank"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>isBlank (str)](#apidoc.element.underscore.string.isBlank)
- description and source-code
```javascript
function isBlank(str) {
  return (/^\s*$/).test(makeString(str));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.join"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>join ()](#apidoc.element.underscore.string.join)
- description and source-code
```javascript
function join() {
  var args = slice.call(arguments),
    separator = args.shift();

  return args.join(makeString(separator));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.levenshtein"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>levenshtein (str1, str2)](#apidoc.element.underscore.string.levenshtein)
- description and source-code
```javascript
function levenshtein(str1, str2) {
  'use strict';
  str1 = makeString(str1);
  str2 = makeString(str2);

  // Short cut cases
  if (str1 === str2) return 0;
  if (!str1 || !str2) return Math.max(str1.length, str2.length);

  // two rows
  var prevRow = new Array(str2.length + 1);

  // initialise previous row
  for (var i = 0; i < prevRow.length; ++i) {
    prevRow[i] = i;
  }

  // calculate current row distance from previous row
  for (i = 0; i < str1.length; ++i) {
    var nextCol = i + 1;

    for (var j = 0; j < str2.length; ++j) {
      var curCol = nextCol;

      // substution
      nextCol = prevRow[j] + ( (str1.charAt(i) === str2.charAt(j)) ? 0 : 1 );
      // insertion
      var tmp = curCol + 1;
      if (nextCol > tmp) {
        nextCol = tmp;
      }
      // deletion
      tmp = prevRow[j + 1] + 1;
      if (nextCol > tmp) {
        nextCol = tmp;
      }

      // copy current col value into previous (in preparation for next iteration)
      prevRow[j] = curCol;
    }

    // copy last col value into previous (in preparation for next iteration)
    prevRow[j] = nextCol;
  }

  return nextCol;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.lines"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>lines (str)](#apidoc.element.underscore.string.lines)
- description and source-code
```javascript
function lines(str) {
  if (str == null) return [];
  return String(str).split(/\r\n?|\n/);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.ljust"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>ljust (str, length, padStr)](#apidoc.element.underscore.string.ljust)
- description and source-code
```javascript
function rpad(str, length, padStr) {
  return pad(str, length, padStr, 'right');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.lpad"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>lpad (str, length, padStr)](#apidoc.element.underscore.string.lpad)
- description and source-code
```javascript
function lpad(str, length, padStr) {
  return pad(str, length, padStr);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.lrpad"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>lrpad (str, length, padStr)](#apidoc.element.underscore.string.lrpad)
- description and source-code
```javascript
function lrpad(str, length, padStr) {
  return pad(str, length, padStr, 'both');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.lstrip"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>lstrip (str, characters)](#apidoc.element.underscore.string.lstrip)
- description and source-code
```javascript
function ltrim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrimLeft) return nativeTrimLeft.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp('^' + characters + '+'), '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.ltrim"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>ltrim (str, characters)](#apidoc.element.underscore.string.ltrim)
- description and source-code
```javascript
function ltrim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrimLeft) return nativeTrimLeft.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp('^' + characters + '+'), '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.map"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>map (str, callback)](#apidoc.element.underscore.string.map)
- description and source-code
```javascript
map = function (str, callback) {
  str = makeString(str);

  if (str.length === 0 || typeof callback !== 'function') return str;

  return str.replace(/./g, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.mapChars"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>mapChars (str, callback)](#apidoc.element.underscore.string.mapChars)
- description and source-code
```javascript
mapChars = function (str, callback) {
  str = makeString(str);

  if (str.length === 0 || typeof callback !== 'function') return str;

  return str.replace(/./g, callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.naturalCmp"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>naturalCmp (str1, str2)](#apidoc.element.underscore.string.naturalCmp)
- description and source-code
```javascript
function naturalCmp(str1, str2) {
  if (str1 == str2) return 0;
  if (!str1) return -1;
  if (!str2) return 1;

  var cmpRegex = /(\.\d+|\d+|\D+)/g,
    tokens1 = String(str1).match(cmpRegex),
    tokens2 = String(str2).match(cmpRegex),
    count = Math.min(tokens1.length, tokens2.length);

  for (var i = 0; i < count; i++) {
    var a = tokens1[i],
      b = tokens2[i];

    if (a !== b) {
      var num1 = +a;
      var num2 = +b;
      if (num1 === num1 && num2 === num2) {
        return num1 > num2 ? 1 : -1;
      }
      return a < b ? -1 : 1;
    }
  }

  if (tokens1.length != tokens2.length)
    return tokens1.length - tokens2.length;

  return str1 < str2 ? -1 : 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.numberFormat"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>numberFormat (number, dec, dsep, tsep)](#apidoc.element.underscore.string.numberFormat)
- description and source-code
```javascript
function numberFormat(number, dec, dsep, tsep) {
  if (isNaN(number) || number == null) return '';

  number = number.toFixed(~~dec);
  tsep = typeof tsep == 'string' ? tsep : ',';

  var parts = number.split('.'),
    fnums = parts[0],
    decimals = parts[1] ? (dsep || '.') + parts[1] : '';

  return fnums.replace(/(\d)(?=(?:\d{3})+$)/g, '$1' + tsep) + decimals;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.pad"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>pad (str, length, padStr, type)](#apidoc.element.underscore.string.pad)
- description and source-code
```javascript
function pad(str, length, padStr, type) {
  str = makeString(str);
  length = ~~length;

  var padlen = 0;

  if (!padStr)
    padStr = ' ';
  else if (padStr.length > 1)
    padStr = padStr.charAt(0);

  switch (type) {
  case 'right':
    padlen = length - str.length;
    return str + strRepeat(padStr, padlen);
  case 'both':
    padlen = length - str.length;
    return strRepeat(padStr, Math.ceil(padlen / 2)) + str + strRepeat(padStr, Math.floor(padlen / 2));
  default: // 'left'
    padlen = length - str.length;
    return strRepeat(padStr, padlen) + str;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.pred"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>pred (str)](#apidoc.element.underscore.string.pred)
- description and source-code
```javascript
function succ(str) {
  return adjacent(str, -1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.prune"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>prune (str, length, pruneStr)](#apidoc.element.underscore.string.prune)
- description and source-code
```javascript
function prune(str, length, pruneStr) {
  str = makeString(str);
  length = ~~length;
  pruneStr = pruneStr != null ? String(pruneStr) : '...';

  if (str.length <= length) return str;

  var tmpl = function(c) {
      return c.toUpperCase() !== c.toLowerCase() ? 'A' : ' ';
    },
    template = str.slice(0, length + 1).replace(/.(?=\W*\w*$)/g, tmpl); // 'Hello, world' -> 'HellAA AAAAA'

  if (template.slice(template.length - 2).match(/\w\w/))
    template = template.replace(/\s*\S+$/, '');
  else
    template = rtrim(template.slice(0, template.length - 1));

  return (template + pruneStr).length > str.length ? str : str.slice(0, template.length) + pruneStr;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.q"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>q (str, quoteChar)](#apidoc.element.underscore.string.q)
- description and source-code
```javascript
function quote(str, quoteChar) {
  return surround(str, quoteChar || '"');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.quote"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>quote (str, quoteChar)](#apidoc.element.underscore.string.quote)
- description and source-code
```javascript
function quote(str, quoteChar) {
  return surround(str, quoteChar || '"');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.repeat"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>repeat (str, qty, separator)](#apidoc.element.underscore.string.repeat)
- description and source-code
```javascript
function repeat(str, qty, separator) {
  str = makeString(str);

  qty = ~~qty;

  // using faster implementation if separator is not needed;
  if (separator == null) return strRepeat(str, qty);

  // this one is about 300x slower in Google Chrome
<span class="apidocCodeCommentSpan">  /*eslint no-empty: 0*/
</span>  for (var repeat = []; qty > 0; repeat[--qty] = str) {}
  return repeat.join(separator);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.replaceAll"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>replaceAll (str, find, replace, ignorecase)](#apidoc.element.underscore.string.replaceAll)
- description and source-code
```javascript
function replaceAll(str, find, replace, ignorecase) {
  var flags = (ignorecase === true)?'gi':'g';
  var reg = new RegExp(find, flags);

  return makeString(str).replace(reg, replace);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.reverse"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>reverse (str)](#apidoc.element.underscore.string.reverse)
- description and source-code
```javascript
function reverse(str) {
  return chars(str).reverse().join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.rjust"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>rjust (str, length, padStr)](#apidoc.element.underscore.string.rjust)
- description and source-code
```javascript
function lpad(str, length, padStr) {
  return pad(str, length, padStr);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.rpad"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>rpad (str, length, padStr)](#apidoc.element.underscore.string.rpad)
- description and source-code
```javascript
function rpad(str, length, padStr) {
  return pad(str, length, padStr, 'right');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.rstrip"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>rstrip (str, characters)](#apidoc.element.underscore.string.rstrip)
- description and source-code
```javascript
function rtrim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrimRight) return nativeTrimRight.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp(characters + '+$'), '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.rtrim"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>rtrim (str, characters)](#apidoc.element.underscore.string.rtrim)
- description and source-code
```javascript
function rtrim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrimRight) return nativeTrimRight.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp(characters + '+$'), '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.slugify"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>slugify (str)](#apidoc.element.underscore.string.slugify)
- description and source-code
```javascript
function slugify(str) {
  return trim(dasherize(cleanDiacritics(str).replace(/[^\w\s-]/g, '-').toLowerCase()), '-');
}
```
- example usage
```shell
...
'''shell
    meteor add underscorestring:underscore.string
'''

and you'll be able to access the library with the ***s*** global from both the server and the client.

'''javascript
s.slugify("Hello world!");
// => hello-world

s("   epeli  ").trim().capitalize().value();
// => "Epeli"
'''

[Meteor]: http://www.meteor.com/
...
```

#### <a name="apidoc.element.underscore.string.splice"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>splice (str, i, howmany, substr)](#apidoc.element.underscore.string.splice)
- description and source-code
```javascript
function splice(str, i, howmany, substr) {
  var arr = chars(str);
  arr.splice(~~i, ~~howmany, substr);
  return arr.join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.sprintf"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>sprintf ()](#apidoc.element.underscore.string.sprintf)
- description and source-code
```javascript
function deprecated() {
  warned = exports.printDeprecationMessage(msg, warned, deprecated);
  if (new.target) {
    return Reflect.construct(fn, arguments, new.target);
  }
  return fn.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.startsWith"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>startsWith (str, starts, position)](#apidoc.element.underscore.string.startsWith)
- description and source-code
```javascript
function startsWith(str, starts, position) {
  str = makeString(str);
  starts = '' + starts;
  position = position == null ? 0 : Math.min(toPositive(position), str.length);
  return str.lastIndexOf(starts, position) === position;
}
```
- example usage
```shell
...
    npm install underscore.string.fp

'''javascript
var S = require('underscore.string.fp');
var filter = require('lodash-fp').filter;
var filter = require('ramda').filter;

filter(S.startsWith('.'), [
  '.vimrc',
  'foo.md',
  '.zshrc'
]);
// => ['.vimrc', '.zshrc']
'''
...
```

#### <a name="apidoc.element.underscore.string.strLeft"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>strLeft (str, sep)](#apidoc.element.underscore.string.strLeft)
- description and source-code
```javascript
function strLeft(str, sep) {
  str = makeString(str);
  sep = makeString(sep);
  var pos = !sep ? -1 : str.indexOf(sep);
  return~ pos ? str.slice(0, pos) : str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.strLeftBack"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>strLeftBack (str, sep)](#apidoc.element.underscore.string.strLeftBack)
- description and source-code
```javascript
function strLeftBack(str, sep) {
  str = makeString(str);
  sep = makeString(sep);
  var pos = str.lastIndexOf(sep);
  return~ pos ? str.slice(0, pos) : str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.strRight"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>strRight (str, sep)](#apidoc.element.underscore.string.strRight)
- description and source-code
```javascript
function strRight(str, sep) {
  str = makeString(str);
  sep = makeString(sep);
  var pos = !sep ? -1 : str.indexOf(sep);
  return~ pos ? str.slice(pos + sep.length, str.length) : str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.strRightBack"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>strRightBack (str, sep)](#apidoc.element.underscore.string.strRightBack)
- description and source-code
```javascript
function strRightBack(str, sep) {
  str = makeString(str);
  sep = makeString(sep);
  var pos = !sep ? -1 : str.lastIndexOf(sep);
  return~ pos ? str.slice(pos + sep.length, str.length) : str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.strip"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>strip (str, characters)](#apidoc.element.underscore.string.strip)
- description and source-code
```javascript
function trim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrim) return nativeTrim.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp('^' + characters + '+|' + characters + '+$', 'g'), '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.stripTags"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>stripTags (str)](#apidoc.element.underscore.string.stripTags)
- description and source-code
```javascript
function stripTags(str) {
  return makeString(str).replace(/<\/?[^>]+>/g, '');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.succ"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>succ (str)](#apidoc.element.underscore.string.succ)
- description and source-code
```javascript
function succ(str) {
  return adjacent(str, 1);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.surround"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>surround (str, wrapper)](#apidoc.element.underscore.string.surround)
- description and source-code
```javascript
function surround(str, wrapper) {
  return [wrapper, str, wrapper].join('');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.swapCase"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>swapCase (str)](#apidoc.element.underscore.string.swapCase)
- description and source-code
```javascript
function swapCase(str) {
  return makeString(str).replace(/\S/g, function(c) {
    return c === c.toUpperCase() ? c.toLowerCase() : c.toUpperCase();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.titleize"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>titleize (str)](#apidoc.element.underscore.string.titleize)
- description and source-code
```javascript
function titleize(str) {
  return makeString(str).toLowerCase().replace(/(?:^|\s|-)\S/g, function(c) {
    return c.toUpperCase();
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toBool"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toBool (str, trueValues, falseValues)](#apidoc.element.underscore.string.toBool)
- description and source-code
```javascript
function toBoolean(str, trueValues, falseValues) {
  if (typeof str === 'number') str = '' + str;
  if (typeof str !== 'string') return !!str;
  str = trim(str);
  if (boolMatch(str, trueValues || ['true', '1'])) return true;
  if (boolMatch(str, falseValues || ['false', '0'])) return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toBoolean"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toBoolean (str, trueValues, falseValues)](#apidoc.element.underscore.string.toBoolean)
- description and source-code
```javascript
function toBoolean(str, trueValues, falseValues) {
  if (typeof str === 'number') str = '' + str;
  if (typeof str !== 'string') return !!str;
  str = trim(str);
  if (boolMatch(str, trueValues || ['true', '1'])) return true;
  if (boolMatch(str, falseValues || ['false', '0'])) return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toNumber"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toNumber (num, precision)](#apidoc.element.underscore.string.toNumber)
- description and source-code
```javascript
function toNumber(num, precision) {
  if (num == null) return 0;
  var factor = Math.pow(10, isFinite(precision) ? precision : 0);
  return Math.round(num * factor) / factor;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toSentence"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toSentence (array, separator, lastSeparator, serial)](#apidoc.element.underscore.string.toSentence)
- description and source-code
```javascript
function toSentence(array, separator, lastSeparator, serial) {
  separator = separator || ', ';
  lastSeparator = lastSeparator || ' and ';
  var a = array.slice(),
    lastMember = a.pop();

  if (array.length > 2 && serial) lastSeparator = rtrim(separator) + lastSeparator;

  return a.length ? a.join(separator) + lastSeparator + lastMember : lastMember;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toSentenceSerial"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toSentenceSerial (array, sep, lastSep)](#apidoc.element.underscore.string.toSentenceSerial)
- description and source-code
```javascript
function toSentenceSerial(array, sep, lastSep) {
  return toSentence(array, sep, lastSep, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.toString"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>toString ()](#apidoc.element.underscore.string.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.trim"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>trim (str, characters)](#apidoc.element.underscore.string.trim)
- description and source-code
```javascript
function trim(str, characters) {
  str = makeString(str);
  if (!characters && nativeTrim) return nativeTrim.call(str);
  characters = defaultToWhiteSpace(characters);
  return str.replace(new RegExp('^' + characters + '+|' + characters + '+$', 'g'), '');
}
```
- example usage
```shell
...
'''

or load the full library to enable chaining

'''javascript
var s = require("underscore.string");

s("   epeli  ").trim().capitalize().value();
// => "Epeli"
'''

but especially when using with [Browserify][] the individual function approach
is recommended because using it you only add those functions to your bundle you
use.
...
```

#### <a name="apidoc.element.underscore.string.truncate"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>truncate (str, length, truncateStr)](#apidoc.element.underscore.string.truncate)
- description and source-code
```javascript
function truncate(str, length, truncateStr) {
  str = makeString(str);
  truncateStr = truncateStr || '...';
  length = ~~length;
  return str.length > length ? str.slice(0, length) + truncateStr : str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.underscored"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>underscored (str)](#apidoc.element.underscore.string.underscored)
- description and source-code
```javascript
function underscored(str) {
  return trim(str).replace(/([a-z\d])([A-Z]+)/g, '$1_$2').replace(/[-\s]+/g, '_').toLowerCase();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.unescapeHTML"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>unescapeHTML (str)](#apidoc.element.underscore.string.unescapeHTML)
- description and source-code
```javascript
function unescapeHTML(str) {
  return makeString(str).replace(/\&([^;]+);/g, function(entity, entityCode) {
    var match;

    if (entityCode in htmlEntities) {
      return htmlEntities[entityCode];
<span class="apidocCodeCommentSpan">    /*eslint no-cond-assign: 0*/
</span>    } else if (match = entityCode.match(/^#x([\da-fA-F]+)$/)) {
      return String.fromCharCode(parseInt(match[1], 16));
    /*eslint no-cond-assign: 0*/
    } else if (match = entityCode.match(/^#(\d+)$/)) {
      return String.fromCharCode(~~match[1]);
    } else {
      return entity;
    }
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.unquote"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>unquote (str, quoteChar)](#apidoc.element.underscore.string.unquote)
- description and source-code
```javascript
function unquote(str, quoteChar) {
  quoteChar = quoteChar || '"';
  if (str[0] === quoteChar && str[str.length - 1] === quoteChar)
    return str.slice(1, str.length - 1);
  else return str;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.vsprintf"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>vsprintf ()](#apidoc.element.underscore.string.vsprintf)
- description and source-code
```javascript
function deprecated() {
  warned = exports.printDeprecationMessage(msg, warned, deprecated);
  if (new.target) {
    return Reflect.construct(fn, arguments, new.target);
  }
  return fn.apply(this, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.words"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>words (str, delimiter)](#apidoc.element.underscore.string.words)
- description and source-code
```javascript
function words(str, delimiter) {
  if (isBlank(str)) return [];
  return trim(str, delimiter).split(delimiter || /\s+/);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.underscore.string.wrap"></a>[function <span class="apidocSignatureSpan">underscore.string.</span>wrap (str, options)](#apidoc.element.underscore.string.wrap)
- description and source-code
```javascript
function wrap(str, options){
  str = makeString(str);

  options = options || {};

  var width = options.width || 75;
  var seperator = options.seperator || '\n';
  var cut = options.cut || false;
  var preserveSpaces = options.preserveSpaces || false;
  var trailingSpaces = options.trailingSpaces || false;

  var result;

  if(width <= 0){
    return str;
  }

  else if(!cut){

    var words = str.split(' ');
    var current_column = 0;
    result = '';

    while(words.length > 0){

      // if adding a space and the next word would cause this line to be longer than width...
      if(1 + words[0].length + current_column > width){
        //start a new line if this line is not already empty
        if(current_column > 0){
          // add a space at the end of the line is preserveSpaces is true
          if (preserveSpaces){
            result += ' ';
            current_column++;
          }
          // fill the rest of the line with spaces if trailingSpaces option is true
          else if(trailingSpaces){
            while(current_column < width){
              result += ' ';
              current_column++;
            }
          }
          //start new line
          result += seperator;
          current_column = 0;
        }
      }

      // if not at the begining of the line, add a space in front of the word
      if(current_column > 0){
        result += ' ';
        current_column++;
      }

      // tack on the next word, update current column, a pop words array
      result += words[0];
      current_column += words[0].length;
      words.shift();

    }

    // fill the rest of the line with spaces if trailingSpaces option is true
    if(trailingSpaces){
      while(current_column < width){
        result += ' ';
        current_column++;
      }
    }

    return result;

  }

  else {

    var index = 0;
    result = '';

    // walk through each character and add seperators where appropriate
    while(index < str.length){
      if(index % width == 0 && index > 0){
        result += seperator;
      }
      result += str.charAt(index);
      index++;
    }

    // fill the rest of the line with spaces if trailingSpaces option is true
    if(trailingSpaces){
      while(index % width > 0){
        result += ' ';
        index++;
      }
    }

    return result;
  }
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
