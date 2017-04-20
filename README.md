# npmtest-react-hyperscript-helpers

#### basic test coverage for  react-hyperscript-helpers (v1.2.0)  [![npm package](https://img.shields.io/npm/v/npmtest-react-hyperscript-helpers.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-react-hyperscript-helpers) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-react-hyperscript-helpers.svg)](https://travis-ci.org/npmtest/node-npmtest-react-hyperscript-helpers)

#### Terse syntax for hyperscript using react

[![NPM](https://nodei.co/npm/react-hyperscript-helpers.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/react-hyperscript-helpers)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-react-hyperscript-helpers/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-react-hyperscript-helpers/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/test-report.html](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-react-hyperscript-helpers/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-react-hyperscript-helpers/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-react-hyperscript-helpers/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-react-hyperscript-helpers/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-react-hyperscript-helpers/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "react-hyperscript-helpers",
    "version": "1.2.0",
    "description": "Terse syntax for hyperscript using react",
    "main": "./lib/index.js",
    "typings": "./lib/index.d.ts",
    "scripts": {
        "build": "npm run build:babel && npm run build:ts-def",
        "build:babel": "babel src --out-dir lib",
        "build:ts-def": "babel-node ./generate-ts-def.js",
        "lint": "eslint src test",
        "test": "npm run test:mocha && npm run test:tsc",
        "test:mocha": "mocha -c -r babel-core/register ./test/**/*Spec.js",
        "test:tsc": "npm run build && npm run test:tsc:fake-install && npm run test:tsc:compile && npm run test:tsc:cleanup",
        "test:tsc:clean-fake": "rm -f node_modules/react-hyperscript-helpers",
        "test:tsc:fake-install": "npm run test:tsc:clean-fake && ln -s .. node_modules/react-hyperscript-helpers",
        "test:tsc:compile": "tsc test/type-definitions.ts --module commonjs",
        "test:tsc:cleanup": "npm run test:tsc:clean-fake && rm test/type-definitions.js",
        "prepublish": "npm run clean && npm run build",
        "postversion": "git push && git push --tags",
        "clean": "rimraf lib"
    },
    "keywords": [
        "hyperscript",
        "react",
        "jsx",
        "hyperscript-helpers",
        "react-hyperscript",
        "react-hyperscript-helpers"
    ],
    "author": "Tyler Graham <tyler.graham.prog@gmail.com>",
    "repository": "github:Jador/react-hyperscript-helpers",
    "license": "ISC",
    "devDependencies": {
        "babel-cli": "^6.5.1",
        "babel-core": "^6.2.1",
        "babel-preset-es2015": "^6.1.18",
        "babel-preset-stage-2": "^6.1.18",
        "chai": "^3.4.1",
        "eslint": "^2.7.0",
        "eslint-config-airbnb": "^6.2.0",
        "eslint-plugin-react": "^4.2.3",
        "mocha": "^2.3.4",
        "rimraf": "^2.4.4",
        "typescript": "^1.7.5"
    },
    "peerDependencies": {
        "react": ">=0.13.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
