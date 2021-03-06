# npmdoc-xstream

#### basic api documentation for  [xstream (v10.5.0)](https://github.com/staltz/xstream#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-xstream.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-xstream) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-xstream.svg)](https://travis-ci.org/npmdoc/node-npmdoc-xstream)

#### An extremely intuitive, small, and fast functional reactive stream library for JavaScript

[![NPM](https://nodei.co/npm/xstream.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/xstream)

- [https://npmdoc.github.io/node-npmdoc-xstream/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-xstream/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xstream/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xstream/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-xstream/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-xstream/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Andre Staltz",
        "url": "http://andre.staltz.com/"
    },
    "bugs": {
        "url": "https://github.com/staltz/xstream/issues"
    },
    "config": {
        "commitizen": {
            "path": "./node_modules/cz-conventional-changelog"
        }
    },
    "dependencies": {
        "symbol-observable": "^1.0.2"
    },
    "description": "An extremely intuitive, small, and fast functional reactive stream library for JavaScript",
    "devDependencies": {
        "@types/mocha": "^2.2.40",
        "@types/node": "^7.0.12",
        "@types/sinon": "^2.1.2",
        "assert": "1.3.x",
        "browserify": "13.0.x",
        "commitizen": "2.9.x",
        "conventional-changelog": "1.1.x",
        "conventional-changelog-cli": "1.2.x",
        "cz-conventional-changelog": "1.2.x",
        "es6-promise": "4.0.5",
        "google-closure-compiler-js": "^20161201.0.0",
        "markdown-doctest": "0.9.1",
        "markdox": "0.1.10",
        "mkdirp": "0.5.1",
        "mocha": "2.4.5",
        "most": "1.0.3",
        "sinon": "1.16.0",
        "strip-comments": "0.4.4",
        "ts-node": "1.7.2",
        "tsify": "2.0.3",
        "tslint": "4.0.2",
        "typescript": "2.1.5",
        "validate-commit-msg": "2.4.x"
    },
    "directories": {},
    "dist": {
        "shasum": "acf7776cf86f0188e09ebaf3227d847818d1564a",
        "tarball": "https://registry.npmjs.org/xstream/-/xstream-10.5.0.tgz"
    },
    "gitHead": "1512654b6216c39db0fb9a69a8b7732eb4a8b1ef",
    "homepage": "https://github.com/staltz/xstream#readme",
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "cycle"
        },
        {
            "name": "staltz"
        }
    ],
    "name": "xstream",
    "optionalDependencies": {},
    "publishConfig": {
        "access": "public"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/staltz/xstream.git"
    },
    "scripts": {
        "changelog": "conventional-changelog --infile CHANGELOG.md --same-file --release-count 0 --preset angular",
        "check-release": "node tools/check-release.js",
        "commit": "git-cz",
        "compile": "tsc",
        "dist": "browserify index.js --standalone xstream | node tools/strip-comments.js > dist/xstream.js",
        "doctest": "markdown-doctest",
        "extra-docs": "node tools/make-extras.js && rm EXTRA_DOCS.md && cp markdown/generated-extras.md EXTRA_DOCS.md",
        "lint": "tslint -c tslint.json src/**/*.ts src/extra/*.ts",
        "mocha": "mocha tests/*.ts tests/**/*.ts --require ts-node/register",
        "page-content": "npm run compile && rm -rf .ignore/ && mkdirp .ignore/ && npm run changelog && node tools/make-toc.js && node tools/make-factories.js && node tools/make-methods.js && cat markdown/header.md markdown/generated-toc.md markdown/overview.md markdown/generated-factories.md markdown/generated-methods.md markdown/footer.md > .ignore/content.md",
        "postdist": "node tools/minify.js",
        "postreadme": "npm run extra-docs",
        "postversion": "git push origin master && git push origin --tags && npm publish && npm run update-gh-pages",
        "predist": "rm -rf dist/ && mkdirp dist/ && npm run compile",
        "premocha": "npm run compile",
        "prepublish": "npm run compile",
        "preversion": "npm run readme && npm test",
        "readme": "npm run page-content && cat markdown/readme-title.md .ignore/content.md > README.md",
        "release": "./tools/release-if-necessary.sh",
        "release-major": "npm version major -m \"chore(package): release new version\"",
        "release-minor": "npm version minor -m \"chore(package): release new version\"",
        "release-patch": "false",
        "setup-browser-tests": "browserify browser-tests/index.ts -p [ tsify ] > browser-tests/tests-bundle.js",
        "start": "npm install && npm prune",
        "teardown-browser-tests": "rm browser-tests/tests-bundle.js",
        "test": "npm run lint && npm run mocha && npm run doctest",
        "update-gh-pages": "git checkout gh-pages && rm _includes/content.md && cp .ignore/content.md _includes/ && git add --all && if git diff --cached --quiet > /dev/null; then :; else git commit -m \"update site\"; fi && git push origin gh-pages && git checkout master",
        "version": "npm run readme && npm run dist && git add -A"
    },
    "typings": "index.d.ts",
    "version": "10.5.0",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
