# api documentation for  [fortune (v5.1.0)](http://fortune.js.org)  [![npm package](https://img.shields.io/npm/v/npmdoc-fortune.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-fortune) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-fortune.svg)](https://travis-ci.org/npmdoc/node-npmdoc-fortune)
#### Database abstraction layer for data-driven applications.

[![NPM](https://nodei.co/npm/fortune.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/fortune)

- [https://npmdoc.github.io/node-npmdoc-fortune/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-fortune/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-fortune/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-fortune/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-fortune/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-fortune/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bugs": {
        "url": "https://github.com/fortunejs/fortune/issues"
    },
    "dependencies": {
        "error-class": "^2.0.1",
        "event-lite": "^0.1.1",
        "tapdance": "^5.0.3"
    },
    "description": "Database abstraction layer for data-driven applications.",
    "devDependencies": {
        "@tap-format/dot": "^0.2.0",
        "browserify": "^13.3.0",
        "chalk": "^1.1.3",
        "cssnano": "^3.10.0",
        "doc-tree": "^0.12.2",
        "eslint": "^3.13.0",
        "eslint-config-boss": "^1.0.5",
        "fortune-http": "^1.0.3",
        "fortune-ws": "^1.0.2",
        "highlight.js": "^9.9.0",
        "html-minifier": "^3.2.3",
        "inflection": "^1.10.0",
        "istanbul": "^0.4.5",
        "marked": "^0.3.6",
        "mkdirp": "^0.5.1",
        "mustache": "^2.3.0",
        "normalize.css": "^5.0.0",
        "postcss": "^5.2.9",
        "postcss-cssnext": "^2.9.0",
        "postcss-import": "^9.0.0",
        "rimraf": "^2.5.4",
        "tapdance": "^5.0.2",
        "tape-run": "^2.1.5",
        "uglify-js": "^2.7.5"
    },
    "directories": {},
    "dist": {
        "shasum": "f501cdb806fb383938d5885d2e900b8589db120d",
        "tarball": "https://registry.npmjs.org/fortune/-/fortune-5.1.0.tgz"
    },
    "engines": {
        "node": ">=4.6"
    },
    "eslintConfig": {
        "extends": "boss/es5"
    },
    "files": [
        "lib/",
        "dist/*.js",
        "test/",
        "LICENSE"
    ],
    "gitHead": "c7f59b7b23260263de1c51167fbfeab33586ad34",
    "homepage": "http://fortune.js.org",
    "keywords": [
        "database",
        "adapter",
        "data",
        "model",
        "record"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "jacksongariety"
        },
        {
            "name": "sapeien"
        }
    ],
    "name": "fortune",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/fortunejs/fortune.git"
    },
    "scripts": {
        "build": "node website/build && npm run build:browser && npm run build:minified",
        "build:browser": "(node lib/header; browserify lib/global.js) > dist/fortune.js",
        "build:minified": "(node lib/header; cat dist/fortune.js | uglifyjs -cm) > dist/fortune.min.js",
        "coverage": "istanbul cover test",
        "deploy": "./website/deploy.sh",
        "lint": "eslint lib",
        "postpublish": "npm run deploy && npm run tag",
        "prepublish": "npm run test && npm run build",
        "tag": "git tag 'npm v fortune version' && git push origin --tags",
        "test": "npm run lint && npm run test:server && npm run test:browser",
        "test:browser": "browserify test/browser.js | tape-run | tf-dot",
        "test:server": "node test | tf-dot"
    },
    "version": "5.1.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
