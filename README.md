# api documentation for  [broccoli (v1.1.1)](https://github.com/broccolijs/broccoli)  [![npm package](https://img.shields.io/npm/v/npmdoc-broccoli.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-broccoli) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-broccoli.svg)](https://travis-ci.org/npmdoc/node-npmdoc-broccoli)
#### Fast client-side asset builder

[![NPM](https://nodei.co/npm/broccoli.png?downloads=true)](https://www.npmjs.com/package/broccoli)

[![apidoc](https://npmdoc.github.io/node-npmdoc-broccoli/build/screenCapture.buildApidoc.browser.%252Fhome%252Ftravis%252Fbuild%252Fnpmdoc%252Fnode-npmdoc-broccoli%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-broccoli/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-broccoli/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-broccoli/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Jo Liss",
        "email": "joliss42@gmail.com"
    },
    "bugs": {
        "url": "https://github.com/broccolijs/broccoli/issues"
    },
    "dependencies": {
        "broccoli-node-info": "1.1.0",
        "broccoli-slow-trees": "^2.0.0",
        "broccoli-source": "^1.1.0",
        "commander": "^2.5.0",
        "connect": "^3.3.3",
        "copy-dereference": "^1.0.0",
        "findup-sync": "^0.4.2",
        "handlebars": "^4.0.4",
        "heimdalljs-logger": "^0.1.7",
        "mime": "^1.2.11",
        "rimraf": "^2.4.3",
        "rsvp": "^3.0.17",
        "sane": "^1.4.1",
        "tmp": "0.0.28",
        "underscore.string": "^3.2.2"
    },
    "description": "Fast client-side asset builder",
    "devDependencies": {
        "chai": "^3.3.0",
        "chai-as-promised": "^5.1.0",
        "fixturify": "^0.2.0",
        "mocha": "^3.0.0",
        "mocha-jshint": "^2.2.5",
        "multidep": "^2.0.0",
        "semver": "^5.3.0",
        "sinon": "^1.17.1",
        "sinon-chai": "^2.8.0",
        "symlink-or-copy": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "0287e72994363777bdfd4e8c71805125337c2bf7",
        "tarball": "https://registry.npmjs.org/broccoli/-/broccoli-1.1.1.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "51917754fdb10bd1fc9a43012479928d41cbded2",
    "homepage": "https://github.com/broccolijs/broccoli",
    "keywords": [
        "builder",
        "build",
        "frontend",
        "browser",
        "asset",
        "pipeline"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "joliss",
            "email": "joliss42@gmail.com"
        },
        {
            "name": "rwjblue",
            "email": "me@rwjblue.com"
        },
        {
            "name": "stefanpenner",
            "email": "stefan.penner@gmail.com"
        }
    ],
    "name": "broccoli",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/broccolijs/broccoli.git"
    },
    "scripts": {
        "pretest": "multidep test/multidep.json",
        "test": "mocha"
    },
    "version": "1.1.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module broccoli](#apidoc.module.broccoli)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder (outputNode, options)](#apidoc.element.broccoli.Builder)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder.TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Watcher (builder, options)](#apidoc.element.broccoli.Watcher)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>WatcherAdapter (options)](#apidoc.element.broccoli.WatcherAdapter)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>cli ()](#apidoc.element.broccoli.cli)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>getMiddleware (watcher, options)](#apidoc.element.broccoli.getMiddleware)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>loadBrocfile ()](#apidoc.element.broccoli.loadBrocfile)
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.BuildError.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.BuilderError.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.InvalidNodeError.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeSetupError.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeWrapper.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.SourceNodeWrapper.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.TransformNodeWrapper.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Builder.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>Watcher.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>WatcherAdapter.prototype
1.  object <span class="apidocSignatureSpan">broccoli.</span>server

#### [module broccoli.Builder](#apidoc.module.broccoli.Builder)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Builder (outputNode, options)](#apidoc.element.broccoli.Builder.Builder)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper)

#### [module broccoli.Builder.BuildError](#apidoc.module.broccoli.Builder.BuildError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError.BuildError)

#### [module broccoli.Builder.BuildError.prototype](#apidoc.module.broccoli.Builder.BuildError.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.BuildError.prototype.</span>constructor (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError.prototype.constructor)

#### [module broccoli.Builder.BuilderError](#apidoc.module.broccoli.Builder.BuilderError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError.BuilderError)

#### [module broccoli.Builder.BuilderError.prototype](#apidoc.module.broccoli.Builder.BuilderError.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.BuilderError.prototype.</span>constructor (message)](#apidoc.element.broccoli.Builder.BuilderError.prototype.constructor)

#### [module broccoli.Builder.InvalidNodeError](#apidoc.module.broccoli.Builder.InvalidNodeError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError.InvalidNodeError)

#### [module broccoli.Builder.InvalidNodeError.prototype](#apidoc.module.broccoli.Builder.InvalidNodeError.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.InvalidNodeError.prototype.</span>constructor (message)](#apidoc.element.broccoli.Builder.InvalidNodeError.prototype.constructor)

#### [module broccoli.Builder.NodeSetupError](#apidoc.module.broccoli.Builder.NodeSetupError)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError.NodeSetupError)

#### [module broccoli.Builder.NodeSetupError.prototype](#apidoc.module.broccoli.Builder.NodeSetupError.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.NodeSetupError.prototype.</span>constructor (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError.prototype.constructor)

#### [module broccoli.Builder.NodeWrapper](#apidoc.module.broccoli.Builder.NodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper.NodeWrapper)

#### [module broccoli.Builder.NodeWrapper.prototype](#apidoc.module.broccoli.Builder.NodeWrapper.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.NodeWrapper.prototype.</span>formatInstantiationStackForTerminal ()](#apidoc.element.broccoli.Builder.NodeWrapper.prototype.formatInstantiationStackForTerminal)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.NodeWrapper.prototype.</span>toJSON ()](#apidoc.element.broccoli.Builder.NodeWrapper.prototype.toJSON)

#### [module broccoli.Builder.SourceNodeWrapper](#apidoc.module.broccoli.Builder.SourceNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.SourceNodeWrapper)

#### [module broccoli.Builder.SourceNodeWrapper.prototype](#apidoc.module.broccoli.Builder.SourceNodeWrapper.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>build ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.build)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>constructor ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>nodeInfoToJSON ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.nodeInfoToJSON)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>setup (features)](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.setup)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>toString ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.toString)

#### [module broccoli.Builder.TransformNodeWrapper](#apidoc.module.broccoli.Builder.TransformNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.</span>TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.TransformNodeWrapper)

#### [module broccoli.Builder.TransformNodeWrapper.prototype](#apidoc.module.broccoli.Builder.TransformNodeWrapper.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>build ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.build)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>constructor ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.constructor)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>nodeInfoToJSON ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.nodeInfoToJSON)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>setup (features)](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.setup)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>toString ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.toString)

#### [module broccoli.Builder.prototype](#apidoc.module.broccoli.Builder.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>build ()](#apidoc.element.broccoli.Builder.prototype.build)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>checkInputPathsExist ()](#apidoc.element.broccoli.Builder.prototype.checkInputPathsExist)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>cleanup ()](#apidoc.element.broccoli.Builder.prototype.cleanup)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>makeNodeWrapper (node, _stack)](#apidoc.element.broccoli.Builder.prototype.makeNodeWrapper)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>mkTmpDir (nodeWrapper, type)](#apidoc.element.broccoli.Builder.prototype.mkTmpDir)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.Builder.prototype.off)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.Builder.prototype.on)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>setupNodes ()](#apidoc.element.broccoli.Builder.prototype.setupNodes)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>setupTmpDirs ()](#apidoc.element.broccoli.Builder.prototype.setupTmpDirs)
1.  [function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.Builder.prototype.trigger)
1.  object <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>features

#### [module broccoli.Watcher](#apidoc.module.broccoli.Watcher)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>Watcher (builder, options)](#apidoc.element.broccoli.Watcher.Watcher)

#### [module broccoli.Watcher.prototype](#apidoc.module.broccoli.Watcher.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_build ()](#apidoc.element.broccoli.Watcher.prototype._build)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_change ()](#apidoc.element.broccoli.Watcher.prototype._change)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_error (err)](#apidoc.element.broccoli.Watcher.prototype._error)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_quit (err)](#apidoc.element.broccoli.Watcher.prototype._quit)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.Watcher.prototype.off)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.Watcher.prototype.on)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>quit ()](#apidoc.element.broccoli.Watcher.prototype.quit)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>start ()](#apidoc.element.broccoli.Watcher.prototype.start)
1.  [function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.Watcher.prototype.trigger)

#### [module broccoli.WatcherAdapter](#apidoc.module.broccoli.WatcherAdapter)
1.  [function <span class="apidocSignatureSpan">broccoli.</span>WatcherAdapter (options)](#apidoc.element.broccoli.WatcherAdapter.WatcherAdapter)

#### [module broccoli.WatcherAdapter.prototype](#apidoc.module.broccoli.WatcherAdapter.prototype)
1.  [function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.WatcherAdapter.prototype.off)
1.  [function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.WatcherAdapter.prototype.on)
1.  [function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>quit ()](#apidoc.element.broccoli.WatcherAdapter.prototype.quit)
1.  [function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.WatcherAdapter.prototype.trigger)
1.  [function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>watch (watchedPaths)](#apidoc.element.broccoli.WatcherAdapter.prototype.watch)

#### [module broccoli.server](#apidoc.module.broccoli.server)
1.  [function <span class="apidocSignatureSpan">broccoli.server.</span>serve (watcher, host, port)](#apidoc.element.broccoli.server.serve)



# <a name="apidoc.module.broccoli"></a>[module broccoli](#apidoc.module.broccoli)

#### <a name="apidoc.element.broccoli.Builder"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder (outputNode, options)](#apidoc.element.broccoli.Builder)
- description and source-code
```javascript
function Builder(outputNode, options) {
  if (options == null) options = {}

  this.outputNode = outputNode
  this.tmpdir = options.tmpdir // can be null

  this.unwatchedPaths = []
  this.watchedPaths = []

  // nodeWrappers store additional bookkeeping information, such as paths.
  // This array contains them in topological (build) order.
  this.nodeWrappers = []
  // This populates this.nodeWrappers as a side effect
  this.outputNodeWrapper = this.makeNodeWrapper(this.outputNode)

  // Catching missing directories here helps prevent later errors when we set
  // up the watcher.
  this.checkInputPathsExist()

  this.setupTmpDirs()

  // Now that temporary directories are set up, we need to run the rest of the
  // constructor in a try/catch block to clean them up if necessary.
  try {

    this.setupNodes()
    this.outputPath = this.outputNodeWrapper.outputPath
    this.buildId = 0

  } catch (e) {
    this.cleanup()
    throw e
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.BuildError"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError)
- description and source-code
```javascript
function BuildError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // for Chai
    BuilderError.call(this)
    return
  }

  originalError = wrapPrimitiveErrors(originalError)

  // Create heavily augmented message for easy printing to the terminal. Web
  // interfaces should refer to broccoliPayload.originalError.message instead.
  var filePart = ''
  if (originalError.file != null) {
    filePart = originalError.file
    if (originalError.line != null) {
      filePart += ':' + originalError.line
      if (originalError.column != null) {
        // .column is zero-indexed
        filePart += ':' + (originalError.column + 1)
      }
    }
    filePart += ': '
  }
  var instantiationStack = ''
  if (originalError.file == null) {
    // We want to report the instantiation stack only for "unexpected" errors
    // (bugs, internal errors), but not for compiler errors and such. For now,
    // the presence of '.file' serves as a heuristic to distinguish between
    // those cases.
    instantiationStack = nodeWrapper.formatInstantiationStackForTerminal()
  }
  var message = filePart + originalError.message +
    (originalError.treeDir ? '\n        in ' + originalError.treeDir : '') +
    '\n        at ' + nodeWrapper.label +
    instantiationStack

  BuilderError.call(this, message)
  this.stack = originalError.stack

  // This error API can change between minor Broccoli version bumps
  this.broccoliPayload = {
    originalError: originalError, // guaranteed to be error object, not primitive
    originalMessage: originalError.message,
    // node info
    nodeId: nodeWrapper.id,
    nodeLabel: nodeWrapper.label,
    nodeName: nodeWrapper.nodeInfo.name,
    nodeAnnotation: nodeWrapper.nodeInfo.annotation,
    instantiationStack: nodeWrapper.nodeInfo.instantiationStack,
    // error location (if any)
    location: {
      file: originalError.file,
      treeDir: originalError.treeDir,
      line: originalError.line,
      column: originalError.column
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.BuilderError"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError)
- description and source-code
```javascript
function BuilderError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  // Note that ES5 subclasses of BuilderError don't in turn need any special
  // code.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.InvalidNodeError"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError)
- description and source-code
```javascript
function InvalidNodeError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.NodeSetupError"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError)
- description and source-code
```javascript
function NodeSetupError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // Chai calls new NodeSetupError() :(
    BuilderError.call(this)
    return
  }
  originalError = wrapPrimitiveErrors(originalError)
  var message = originalError.message +
    '\nat ' + nodeWrapper.label +
    nodeWrapper.formatInstantiationStackForTerminal()
  BuilderError.call(this, message)
  // The stack will have the original exception name, but that's OK
  this.stack = originalError.stack
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.NodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper)
- description and source-code
```javascript
function NodeWrapper() {
  this.buildState = {}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper)
- description and source-code
```javascript
function SourceNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder.TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper)
- description and source-code
```javascript
function TransformNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Watcher (builder, options)](#apidoc.element.broccoli.Watcher)
- description and source-code
```javascript
function Watcher(builder, options) {
  this.options = options || {}
  if (this.options.debounce == null) this.options.debounce = 100
  this.builder = builder
  this.watcherAdapter = new WatcherAdapter(this.options.saneOptions)
  this.currentBuild = null
  this._rebuildScheduled = false
  this._ready = false
  this._quitting = false
  this._lifetimeDeferred = null
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.WatcherAdapter"></a>[function <span class="apidocSignatureSpan">broccoli.</span>WatcherAdapter (options)](#apidoc.element.broccoli.WatcherAdapter)
- description and source-code
```javascript
function WatcherAdapter(options) {
  this.options = options || {}
  this.options.filter = this.options.filter || defaultFilterFunction
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.cli"></a>[function <span class="apidocSignatureSpan">broccoli.</span>cli ()](#apidoc.element.broccoli.cli)
- description and source-code
```javascript
function broccoliCLI() {
  var actionPerformed = false
  program
    .version(JSON.parse(fs.readFileSync(__dirname + '/../package.json', 'utf8')).version)
    .usage('[options] <command> [<args ...>]')

  program.command('serve')
    .description('start a broccoli server')
    .option('--port <port>', 'the port to bind to [4200]', 4200)
    .option('--host <host>', 'the host to bind to [localhost]', 'localhost')
    .action(function(options) {
      actionPerformed = true
      broccoli.server.serve(new Watcher(getBuilder()), options.host, parseInt(options.port, 10))
    })

  program.command('build <target>')
    .description('output files to target directory')
    .action(function(outputDir) {
      actionPerformed = true
      if (fs.existsSync(outputDir)) {
        console.error(outputDir + '/ already exists; we cannot build into an existing directory')
        process.exit(1)
      }
      var builder = getBuilder()
      builder.build()
        .then(function() {
          copyDereferenceSync(builder.outputPath, outputDir)
        })
        .finally(function () {
          return builder.cleanup()
        })
        .then(function () {
          process.exit(0)
        })
        .catch(function (err) {
          // Should show file and line/col if present
          if (err.file) {
            console.error('File: ' + err.file)
          }
          console.error(err.stack)
          console.error('\nBuild failed')
          process.exit(1)
        })
    })

  program.parse(process.argv)
  if(!actionPerformed) {
    program.outputHelp()
    process.exit(1)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.getMiddleware"></a>[function <span class="apidocSignatureSpan">broccoli.</span>getMiddleware (watcher, options)](#apidoc.element.broccoli.getMiddleware)
- description and source-code
```javascript
function getMiddleware(watcher, options) {
  if (options == null) options = {}
  if (options.autoIndex == null) options.autoIndex = true

  var outputPath = watcher.builder.outputPath

  return function broccoliMiddleware(request, response, next) {
    if (watcher.currentBuild == null) {
      throw new Error('Waiting for initial build to start')
    }
    watcher.currentBuild.then(function() {
      var urlObj = url.parse(request.url)
      var filename = path.join(outputPath, decodeURIComponent(urlObj.pathname))
      var stat, lastModified, type, charset, buffer

      // contains null byte or escapes directory
      if (filename.indexOf('\0') !== -1 || filename.indexOf(outputPath) !== 0) {
        response.writeHead(400)
        response.end()
        return
      }

      try {
        stat = fs.statSync(filename)
      } catch (e) {
        // not found
        next()
        return
      }

      if (stat.isDirectory()) {
        var hasIndex = fs.existsSync(path.join(filename, 'index.html'))

        if (!hasIndex && !options.autoIndex) {
          next()
          return
        }

        // If no trailing slash, redirect. We use path.sep because filename
        // has backslashes on Windows.
        if (filename[filename.length - 1] !== path.sep) {
          urlObj.pathname += '/'
          response.setHeader('Location', url.format(urlObj))
          response.setHeader('Cache-Control', 'private, max-age=0, must-revalidate')
          response.writeHead(301)
          response.end()
          return
        }

        if (!hasIndex) { // implied: options.autoIndex is true
          var context = {
            url: request.url,
            files: fs.readdirSync(filename).sort().map(function (child){
              var stat = fs.statSync(path.join(filename,child)),
                isDir = stat.isDirectory()
              return {
                href: child + (isDir ? '/' : ''),
                type: isDir ? 'dir' : path.extname(child).replace('.', '').toLowerCase()
              }
            }),
            liveReloadPath: options.liveReloadPath
          }
          response.setHeader('Cache-Control', 'private, max-age=0, must-revalidate')
          response.writeHead(200)
          response.end(dirTemplate(context))
          return
        }

        // otherwise serve index.html
        filename += 'index.html'
        stat = fs.statSync(filename)
      }

      lastModified = stat.mtime.toUTCString()
      response.setHeader('Last-Modified', lastModified)
      // nginx style treat last-modified as a tag since browsers echo it back
      if (request.headers['if-modified-since'] === lastModified) {
        response.writeHead(304)
        response.end()
        return
      }

      type = mime.lookup(filename)
      charset = mime.charsets.lookup(type)
      if (charset) {
        type += '; charset=' + charset
      }
      response.setHeader('Cache-Control', 'private, max-age=0, must-revalidate')
      response.setHeader('Content-Length', stat.size)
      response.setHeader('Content-Type', type)

      // read file sync so we don't hold open the file creating a race with
      // the builder (Windows does not allow us to delete while the file is open).
      buffer = fs.readFileSync(filename)
      response.writeHead(200)
      response.end(buffer)
    }, function(buildError) {
      // All errors thrown from builder.build() are guaranteed to be
      // Builder.BuildError instances.
      var context = {
        stack: buildError.stack,
        liveReloadPath: options.liveReloadPath,
        payload: buildError.broccoliPayload
      }
      response.setHeader('Content-Type', 'text/html')
      response.writeHead(500)
      response.end(errorTemplate(context))
    }).catch(function(err) { console.log(err.stack) })
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.loadBrocfile"></a>[function <span class="apidocSignatureSpan">broccoli.</span>loadBrocfile ()](#apidoc.element.broccoli.loadBrocfile)
- description and source-code
```javascript
function loadBrocfile() {
  var brocfile = findup('Brocfile.js', {
    nocase: true
  })

  if (brocfile == null) throw new Error('Brocfile.js not found')

  var baseDir = path.dirname(brocfile)

  // The chdir should perhaps live somewhere else and not be a side effect of
  // this function, or go away entirely
  process.chdir(baseDir)

  var node = require(brocfile)

  return node
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder"></a>[module broccoli.Builder](#apidoc.module.broccoli.Builder)

#### <a name="apidoc.element.broccoli.Builder.Builder"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Builder (outputNode, options)](#apidoc.element.broccoli.Builder.Builder)
- description and source-code
```javascript
function Builder(outputNode, options) {
  if (options == null) options = {}

  this.outputNode = outputNode
  this.tmpdir = options.tmpdir // can be null

  this.unwatchedPaths = []
  this.watchedPaths = []

  // nodeWrappers store additional bookkeeping information, such as paths.
  // This array contains them in topological (build) order.
  this.nodeWrappers = []
  // This populates this.nodeWrappers as a side effect
  this.outputNodeWrapper = this.makeNodeWrapper(this.outputNode)

  // Catching missing directories here helps prevent later errors when we set
  // up the watcher.
  this.checkInputPathsExist()

  this.setupTmpDirs()

  // Now that temporary directories are set up, we need to run the rest of the
  // constructor in a try/catch block to clean them up if necessary.
  try {

    this.setupNodes()
    this.outputPath = this.outputNodeWrapper.outputPath
    this.buildId = 0

  } catch (e) {
    this.cleanup()
    throw e
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.BuildError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError)
- description and source-code
```javascript
function BuildError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // for Chai
    BuilderError.call(this)
    return
  }

  originalError = wrapPrimitiveErrors(originalError)

  // Create heavily augmented message for easy printing to the terminal. Web
  // interfaces should refer to broccoliPayload.originalError.message instead.
  var filePart = ''
  if (originalError.file != null) {
    filePart = originalError.file
    if (originalError.line != null) {
      filePart += ':' + originalError.line
      if (originalError.column != null) {
        // .column is zero-indexed
        filePart += ':' + (originalError.column + 1)
      }
    }
    filePart += ': '
  }
  var instantiationStack = ''
  if (originalError.file == null) {
    // We want to report the instantiation stack only for "unexpected" errors
    // (bugs, internal errors), but not for compiler errors and such. For now,
    // the presence of '.file' serves as a heuristic to distinguish between
    // those cases.
    instantiationStack = nodeWrapper.formatInstantiationStackForTerminal()
  }
  var message = filePart + originalError.message +
    (originalError.treeDir ? '\n        in ' + originalError.treeDir : '') +
    '\n        at ' + nodeWrapper.label +
    instantiationStack

  BuilderError.call(this, message)
  this.stack = originalError.stack

  // This error API can change between minor Broccoli version bumps
  this.broccoliPayload = {
    originalError: originalError, // guaranteed to be error object, not primitive
    originalMessage: originalError.message,
    // node info
    nodeId: nodeWrapper.id,
    nodeLabel: nodeWrapper.label,
    nodeName: nodeWrapper.nodeInfo.name,
    nodeAnnotation: nodeWrapper.nodeInfo.annotation,
    instantiationStack: nodeWrapper.nodeInfo.instantiationStack,
    // error location (if any)
    location: {
      file: originalError.file,
      treeDir: originalError.treeDir,
      line: originalError.line,
      column: originalError.column
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.BuilderError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError)
- description and source-code
```javascript
function BuilderError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  // Note that ES5 subclasses of BuilderError don't in turn need any special
  // code.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.InvalidNodeError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError)
- description and source-code
```javascript
function InvalidNodeError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.NodeSetupError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError)
- description and source-code
```javascript
function NodeSetupError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // Chai calls new NodeSetupError() :(
    BuilderError.call(this)
    return
  }
  originalError = wrapPrimitiveErrors(originalError)
  var message = originalError.message +
    '\nat ' + nodeWrapper.label +
    nodeWrapper.formatInstantiationStackForTerminal()
  BuilderError.call(this, message)
  // The stack will have the original exception name, but that's OK
  this.stack = originalError.stack
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.NodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper)
- description and source-code
```javascript
function NodeWrapper() {
  this.buildState = {}
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper)
- description and source-code
```javascript
function SourceNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper)
- description and source-code
```javascript
function TransformNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.BuildError"></a>[module broccoli.Builder.BuildError](#apidoc.module.broccoli.Builder.BuildError)

#### <a name="apidoc.element.broccoli.Builder.BuildError.BuildError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuildError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError.BuildError)
- description and source-code
```javascript
function BuildError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // for Chai
    BuilderError.call(this)
    return
  }

  originalError = wrapPrimitiveErrors(originalError)

  // Create heavily augmented message for easy printing to the terminal. Web
  // interfaces should refer to broccoliPayload.originalError.message instead.
  var filePart = ''
  if (originalError.file != null) {
    filePart = originalError.file
    if (originalError.line != null) {
      filePart += ':' + originalError.line
      if (originalError.column != null) {
        // .column is zero-indexed
        filePart += ':' + (originalError.column + 1)
      }
    }
    filePart += ': '
  }
  var instantiationStack = ''
  if (originalError.file == null) {
    // We want to report the instantiation stack only for "unexpected" errors
    // (bugs, internal errors), but not for compiler errors and such. For now,
    // the presence of '.file' serves as a heuristic to distinguish between
    // those cases.
    instantiationStack = nodeWrapper.formatInstantiationStackForTerminal()
  }
  var message = filePart + originalError.message +
    (originalError.treeDir ? '\n        in ' + originalError.treeDir : '') +
    '\n        at ' + nodeWrapper.label +
    instantiationStack

  BuilderError.call(this, message)
  this.stack = originalError.stack

  // This error API can change between minor Broccoli version bumps
  this.broccoliPayload = {
    originalError: originalError, // guaranteed to be error object, not primitive
    originalMessage: originalError.message,
    // node info
    nodeId: nodeWrapper.id,
    nodeLabel: nodeWrapper.label,
    nodeName: nodeWrapper.nodeInfo.name,
    nodeAnnotation: nodeWrapper.nodeInfo.annotation,
    instantiationStack: nodeWrapper.nodeInfo.instantiationStack,
    // error location (if any)
    location: {
      file: originalError.file,
      treeDir: originalError.treeDir,
      line: originalError.line,
      column: originalError.column
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.BuildError.prototype"></a>[module broccoli.Builder.BuildError.prototype](#apidoc.module.broccoli.Builder.BuildError.prototype)

#### <a name="apidoc.element.broccoli.Builder.BuildError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.BuildError.prototype.</span>constructor (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.BuildError.prototype.constructor)
- description and source-code
```javascript
function BuildError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // for Chai
    BuilderError.call(this)
    return
  }

  originalError = wrapPrimitiveErrors(originalError)

  // Create heavily augmented message for easy printing to the terminal. Web
  // interfaces should refer to broccoliPayload.originalError.message instead.
  var filePart = ''
  if (originalError.file != null) {
    filePart = originalError.file
    if (originalError.line != null) {
      filePart += ':' + originalError.line
      if (originalError.column != null) {
        // .column is zero-indexed
        filePart += ':' + (originalError.column + 1)
      }
    }
    filePart += ': '
  }
  var instantiationStack = ''
  if (originalError.file == null) {
    // We want to report the instantiation stack only for "unexpected" errors
    // (bugs, internal errors), but not for compiler errors and such. For now,
    // the presence of '.file' serves as a heuristic to distinguish between
    // those cases.
    instantiationStack = nodeWrapper.formatInstantiationStackForTerminal()
  }
  var message = filePart + originalError.message +
    (originalError.treeDir ? '\n        in ' + originalError.treeDir : '') +
    '\n        at ' + nodeWrapper.label +
    instantiationStack

  BuilderError.call(this, message)
  this.stack = originalError.stack

  // This error API can change between minor Broccoli version bumps
  this.broccoliPayload = {
    originalError: originalError, // guaranteed to be error object, not primitive
    originalMessage: originalError.message,
    // node info
    nodeId: nodeWrapper.id,
    nodeLabel: nodeWrapper.label,
    nodeName: nodeWrapper.nodeInfo.name,
    nodeAnnotation: nodeWrapper.nodeInfo.annotation,
    instantiationStack: nodeWrapper.nodeInfo.instantiationStack,
    // error location (if any)
    location: {
      file: originalError.file,
      treeDir: originalError.treeDir,
      line: originalError.line,
      column: originalError.column
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.BuilderError"></a>[module broccoli.Builder.BuilderError](#apidoc.module.broccoli.Builder.BuilderError)

#### <a name="apidoc.element.broccoli.Builder.BuilderError.BuilderError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>BuilderError (message)](#apidoc.element.broccoli.Builder.BuilderError.BuilderError)
- description and source-code
```javascript
function BuilderError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  // Note that ES5 subclasses of BuilderError don't in turn need any special
  // code.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.BuilderError.prototype"></a>[module broccoli.Builder.BuilderError.prototype](#apidoc.module.broccoli.Builder.BuilderError.prototype)

#### <a name="apidoc.element.broccoli.Builder.BuilderError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.BuilderError.prototype.</span>constructor (message)](#apidoc.element.broccoli.Builder.BuilderError.prototype.constructor)
- description and source-code
```javascript
function BuilderError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  // Note that ES5 subclasses of BuilderError don't in turn need any special
  // code.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.InvalidNodeError"></a>[module broccoli.Builder.InvalidNodeError](#apidoc.module.broccoli.Builder.InvalidNodeError)

#### <a name="apidoc.element.broccoli.Builder.InvalidNodeError.InvalidNodeError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>InvalidNodeError (message)](#apidoc.element.broccoli.Builder.InvalidNodeError.InvalidNodeError)
- description and source-code
```javascript
function InvalidNodeError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.InvalidNodeError.prototype"></a>[module broccoli.Builder.InvalidNodeError.prototype](#apidoc.module.broccoli.Builder.InvalidNodeError.prototype)

#### <a name="apidoc.element.broccoli.Builder.InvalidNodeError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.InvalidNodeError.prototype.</span>constructor (message)](#apidoc.element.broccoli.Builder.InvalidNodeError.prototype.constructor)
- description and source-code
```javascript
function InvalidNodeError(message) {
  // Subclassing Error in ES5 is non-trivial because reasons, so we need this
  // extra constructor logic from http://stackoverflow.com/a/17891099/525872.
  var temp = Error.apply(this, arguments)
  // Need to assign temp.name for correct error class in .stack and .message
  temp.name = this.name = this.constructor.name
  this.stack = temp.stack
  this.message = temp.message
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.NodeSetupError"></a>[module broccoli.Builder.NodeSetupError](#apidoc.module.broccoli.Builder.NodeSetupError)

#### <a name="apidoc.element.broccoli.Builder.NodeSetupError.NodeSetupError"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeSetupError (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError.NodeSetupError)
- description and source-code
```javascript
function NodeSetupError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // Chai calls new NodeSetupError() :(
    BuilderError.call(this)
    return
  }
  originalError = wrapPrimitiveErrors(originalError)
  var message = originalError.message +
    '\nat ' + nodeWrapper.label +
    nodeWrapper.formatInstantiationStackForTerminal()
  BuilderError.call(this, message)
  // The stack will have the original exception name, but that's OK
  this.stack = originalError.stack
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.NodeSetupError.prototype"></a>[module broccoli.Builder.NodeSetupError.prototype](#apidoc.module.broccoli.Builder.NodeSetupError.prototype)

#### <a name="apidoc.element.broccoli.Builder.NodeSetupError.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.NodeSetupError.prototype.</span>constructor (originalError, nodeWrapper)](#apidoc.element.broccoli.Builder.NodeSetupError.prototype.constructor)
- description and source-code
```javascript
function NodeSetupError(originalError, nodeWrapper) {
  if (nodeWrapper == null) { // Chai calls new NodeSetupError() :(
    BuilderError.call(this)
    return
  }
  originalError = wrapPrimitiveErrors(originalError)
  var message = originalError.message +
    '\nat ' + nodeWrapper.label +
    nodeWrapper.formatInstantiationStackForTerminal()
  BuilderError.call(this, message)
  // The stack will have the original exception name, but that's OK
  this.stack = originalError.stack
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.NodeWrapper"></a>[module broccoli.Builder.NodeWrapper](#apidoc.module.broccoli.Builder.NodeWrapper)

#### <a name="apidoc.element.broccoli.Builder.NodeWrapper.NodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>NodeWrapper ()](#apidoc.element.broccoli.Builder.NodeWrapper.NodeWrapper)
- description and source-code
```javascript
function NodeWrapper() {
  this.buildState = {}
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.NodeWrapper.prototype"></a>[module broccoli.Builder.NodeWrapper.prototype](#apidoc.module.broccoli.Builder.NodeWrapper.prototype)

#### <a name="apidoc.element.broccoli.Builder.NodeWrapper.prototype.formatInstantiationStackForTerminal"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.NodeWrapper.prototype.</span>formatInstantiationStackForTerminal ()](#apidoc.element.broccoli.Builder.NodeWrapper.prototype.formatInstantiationStackForTerminal)
- description and source-code
```javascript
formatInstantiationStackForTerminal = function () {
  return '\n-~- created here: -~-\n' + this.nodeInfo.instantiationStack + '\n-~- (end) -~-'
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.NodeWrapper.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.NodeWrapper.prototype.</span>toJSON ()](#apidoc.element.broccoli.Builder.NodeWrapper.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return undefinedToNull({
    id: this.id,
    nodeInfo: this.nodeInfoToJSON(),
    buildState: this.buildState,
    label: this.label,
    inputNodeWrappers: this.inputNodeWrappers.map(function(nw) { return nw.id }),
    cachePath: this.cachePath,
    outputPath: this.outputPath
    // leave out node, originalNode, inputPaths (redundant), build
  })
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.SourceNodeWrapper"></a>[module broccoli.Builder.SourceNodeWrapper](#apidoc.module.broccoli.Builder.SourceNodeWrapper)

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.SourceNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>SourceNodeWrapper ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.SourceNodeWrapper)
- description and source-code
```javascript
function SourceNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.SourceNodeWrapper.prototype"></a>[module broccoli.Builder.SourceNodeWrapper.prototype](#apidoc.module.broccoli.Builder.SourceNodeWrapper.prototype)

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.build"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>build ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.build)
- description and source-code
```javascript
build = function () {
  // We only check here that the sourceDirectory exists and is a directory
  try {
    if (!fs.statSync(this.nodeInfo.sourceDirectory).isDirectory()) {
      throw new Error('Not a directory')
    }
  } catch (err) { // stat might throw, or we might throw
    err.file = this.nodeInfo.sourceDirectory
    // fs.stat augments error message with file name, but that's redundant
    // with our err.file, so we strip it
    err.message = err.message.replace(/, stat '[^'\n]*'$/m, '')
    throw err
  }

  this.buildState.selfTime = 0
  this.buildState.totalTime = 0
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>constructor ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.constructor)
- description and source-code
```javascript
function SourceNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.nodeInfoToJSON"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>nodeInfoToJSON ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.nodeInfoToJSON)
- description and source-code
```javascript
nodeInfoToJSON = function () {
  return undefinedToNull({
    nodeType: 'source',
    sourceDirectory: this.nodeInfo.sourceDirectory,
    watched: this.nodeInfo.watched,
    name: this.nodeInfo.name,
    annotation: this.nodeInfo.annotation
    // leave out instantiationStack
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.setup"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>setup (features)](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.setup)
- description and source-code
```javascript
setup = function (features) {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.toString"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.SourceNodeWrapper.prototype.</span>toString ()](#apidoc.element.broccoli.Builder.SourceNodeWrapper.prototype.toString)
- description and source-code
```javascript
toString = function () {
  var hint = this.nodeInfo.sourceDirectory +
    (this.nodeInfo.watched ? '' : ' (unwatched)')
  return '[NodeWrapper:' + this.id + ' ' + hint + ']'
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.TransformNodeWrapper"></a>[module broccoli.Builder.TransformNodeWrapper](#apidoc.module.broccoli.Builder.TransformNodeWrapper)

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.TransformNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.</span>TransformNodeWrapper ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.TransformNodeWrapper)
- description and source-code
```javascript
function TransformNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.TransformNodeWrapper.prototype"></a>[module broccoli.Builder.TransformNodeWrapper.prototype](#apidoc.module.broccoli.Builder.TransformNodeWrapper.prototype)

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.build"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>build ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.build)
- description and source-code
```javascript
build = function () {
  var self = this

  var startTime = process.hrtime()

  if (!this.nodeInfo.persistentOutput) {
    rimraf.sync(this.outputPath)
    fs.mkdirSync(this.outputPath)
  }

  return RSVP.resolve(self.callbackObject.build())

    .then(function() {
      var now = process.hrtime()
      // Build time in milliseconds
      self.buildState.selfTime = 1000 * ((now[0] - startTime[0]) + (now[1] - startTime[1]) / 1e9)
      self.buildState.totalTime = self.buildState.selfTime
      for (var i = 0; i < self.inputNodeWrappers.length; i++) {
        self.buildState.totalTime += self.inputNodeWrappers[i].buildState.totalTime
      }
    })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.constructor"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>constructor ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.constructor)
- description and source-code
```javascript
function TransformNodeWrapper() {
  NodeWrapper.apply(this, arguments)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.nodeInfoToJSON"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>nodeInfoToJSON ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.nodeInfoToJSON)
- description and source-code
```javascript
nodeInfoToJSON = function () {
  return undefinedToNull({
    nodeType: 'transform',
    name: this.nodeInfo.name,
    annotation: this.nodeInfo.annotation,
    persistentOutput: this.nodeInfo.persistentOutput,
    needsCache: this.nodeInfo.needsCache
    // leave out instantiationStack (too long), inputNodes, and callbacks
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.setup"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>setup (features)](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.setup)
- description and source-code
```javascript
setup = function (features) {
  this.nodeInfo.setup(features, {
    inputPaths: this.inputPaths,
    outputPath: this.outputPath,
    cachePath: this.cachePath
  })
  this.callbackObject = this.nodeInfo.getCallbackObject()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.toString"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.TransformNodeWrapper.prototype.</span>toString ()](#apidoc.element.broccoli.Builder.TransformNodeWrapper.prototype.toString)
- description and source-code
```javascript
toString = function () {
  var hint = this.label
  hint = this.label
  if (this.inputNodeWrappers) { // a bit defensive to deal with partially-constructed node wrappers
    hint += ' inputNodeWrappers:[' + this.inputNodeWrappers.map(function(nw) { return nw.id }) + ']'
  }
  hint += ' at ' + this.outputPath
  if (this.buildState.selfTime != null) {
    hint += ' (' + Math.round(this.buildState.selfTime) + ' ms)'
  }
  return '[NodeWrapper:' + this.id + ' ' + hint + ']'
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Builder.prototype"></a>[module broccoli.Builder.prototype](#apidoc.module.broccoli.Builder.prototype)

#### <a name="apidoc.element.broccoli.Builder.prototype.build"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>build ()](#apidoc.element.broccoli.Builder.prototype.build)
- description and source-code
```javascript
build = function () {
  var self = this
  this.buildId++
  var promise = RSVP.resolve()
  this.nodeWrappers.forEach(function(nw) {
    // We use '.forEach' instead of 'for' to close nested functions over 'nw'

    // Wipe all buildState objects at the beginning of the build
    nw.buildState = {}

    promise = promise
      .then(function() {
        // We use a nested .then/.catch so that the .catch can only catch errors
        // from this node, but not from previous nodes.
        return RSVP.resolve()
          .then(function() {
            self.trigger('beginNode', nw)
          })
          .then(function() {
            return nw.build()
          })
          .finally(function() {
            self.trigger('endNode', nw)
          })
          .catch(function(err) {
            throw new BuildError(err, nw)
          })
      })
  })
  return promise
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.checkInputPathsExist"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>checkInputPathsExist ()](#apidoc.element.broccoli.Builder.prototype.checkInputPathsExist)
- description and source-code
```javascript
checkInputPathsExist = function () {
  // We might consider checking this.unwatchedPaths as well.
  for (var i = 0; i < this.watchedPaths.length; i++) {
    var isDirectory
    try {
      isDirectory = fs.statSync(this.watchedPaths[i]).isDirectory()
    } catch (err) {
      throw new Builder.BuilderError('Directory not found: ' + this.watchedPaths[i])
    }
    if (!isDirectory) {
      throw new Builder.BuilderError('Not a directory: ' + this.watchedPaths[i])
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.cleanup"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>cleanup ()](#apidoc.element.broccoli.Builder.prototype.cleanup)
- description and source-code
```javascript
cleanup = function () {
  this.builderTmpDirCleanup()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.makeNodeWrapper"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>makeNodeWrapper (node, _stack)](#apidoc.element.broccoli.Builder.prototype.makeNodeWrapper)
- description and source-code
```javascript
makeNodeWrapper = function (node, _stack) {
  if (_stack == null) _stack = []
  var self = this

  // Dedupe nodes reachable through multiple paths
  for (var i = 0; i < this.nodeWrappers.length; i++) {
    if (this.nodeWrappers[i].originalNode === node) {
      return this.nodeWrappers[i]
    }
  }

  // Turn string nodes into WatchedDir nodes
  var originalNode = node // keep original (possibly string) node around for deduping
  if (typeof node === 'string') {
    node = new WatchedDir(node, { annotation: 'string node' })
  }

  // Call node.__broccoliGetInfo__()
  var nodeInfo
  try {
    nodeInfo = broccoliNodeInfo.getNodeInfo(node)
  } catch (e) {
    if (!(e instanceof broccoliNodeInfo.InvalidNodeError)) throw e
    // We don't have the instantiation stack of an invalid node, so to aid
    // debugging, we instead report its parent node
    var messageSuffix = (_stack.length > 0) ?
      '\nused as input node to ' + _stack[_stack.length-1].label +
        _stack[_stack.length-1].formatInstantiationStackForTerminal()
      : '\nused as output node'
    throw new broccoliNodeInfo.InvalidNodeError(e.message + messageSuffix)
  }

  // Compute label, like "Funnel (test suite)"
  var label = nodeInfo.name
  var labelExtras = []
  if (nodeInfo.nodeType === 'source') labelExtras.push(nodeInfo.sourceDirectory)
  if (nodeInfo.annotation != null) labelExtras.push(nodeInfo.annotation)
  if (labelExtras.length > 0) label += ' (' + labelExtras.join('; ') + ')'

  // We start constructing the nodeWrapper here because we'll need the partial
  // nodeWrapper for the _stack. Later we'll add more properties.
  var nodeWrapper = nodeInfo.nodeType === 'transform' ?
    new TransformNodeWrapper : new SourceNodeWrapper
  nodeWrapper.nodeInfo = nodeInfo
  nodeWrapper.originalNode = originalNode
  nodeWrapper.node = node
  nodeWrapper.label = label

  // Detect cycles
  for (i = 0; i < _stack.length; i++) {
    if (_stack[i].node === originalNode) {
      var cycleMessage = 'Cycle in node graph: '
      for (var j = i; j < _stack.length; j++) {
        cycleMessage += _stack[j].label + ' -> '
      }
      cycleMessage += nodeWrapper.label
      throw new BuilderError(cycleMessage)
    }
  }

  // For 'transform' nodes, recurse into the input nodes; for 'source' nodes,
  // record paths.
  var inputNodeWrappers = []
  if (nodeInfo.nodeType === 'transform') {
    var newStack = _stack.concat([nodeWrapper])
    inputNodeWrappers = nodeInfo.inputNodes.map(function(inputNode) {
      return self.makeNodeWrapper(inputNode, newStack)
    })
  } else { // nodeType === 'source'
    if (nodeInfo.watched) {
      this.watchedPaths.push(nodeInfo.sourceDirectory)
    } else {
      this.unwatchedPaths.push(nodeInfo.sourceDirectory)
    }
  }

  // For convenience, all nodeWrappers get an 'inputNodeWrappers' array; for
  // 'source' nodes it's empty.
  nodeWrapper.inputNodeWrappers = inputNodeWrappers

  nodeWrapper.id = this.nodeWrappers.length

  // this.nodeWrappers will contain all the node wrappers in topological
  // order, i.e. each node comes after all its input nodes.
  //
  // It's unfortunate that we're mutating this.nodeWrappers as a side effect,
  // but since we work backwards from the output node to discover all the
  // input nodes, it's harder to do a side-effect-free topological sort.
  this.nodeWrappers.push(nodeWrapper)

  return nodeWrapper
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.mkTmpDir"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>mkTmpDir (nodeWrapper, type)](#apidoc.element.broccoli.Builder.prototype.mkTmpDir)
- description and source-code
```javascript
mkTmpDir = function (nodeWrapper, type) {
  var nameAndAnnotation = nodeWrapper.nodeInfo.name + ' ' + (nodeWrapper.nodeInfo.annotation || '')
  // slugify turns fooBar into foobar, so we call underscored first to
  // preserve word boundaries
  var suffix = underscoreString.underscored(nameAndAnnotation.substr(0, 60))
  suffix = underscoreString.slugify(suffix).replace(/-/g, '_')
  // 1 .. 147 -> '001' .. '147'
  var paddedId = underscoreString.pad('' + nodeWrapper.id, ('' + this.nodeWrappers.length).length, '0')
  var dirname = type + '-' + paddedId + '-' + suffix
  var tmpDir = path.join(this.builderTmpDir, dirname)
  fs.mkdirSync(tmpDir)
  return tmpDir
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.off"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.Builder.prototype.off)
- description and source-code
```javascript
function off(eventName, callback) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      index = undefined;

  if (!callback) {
    allCallbacks[eventName] = [];
    return;
  }

  callbacks = allCallbacks[eventName];

  index = indexOf(callbacks, callback);

  if (index !== -1) {
    callbacks.splice(index, 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.on"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.Builder.prototype.on)
- description and source-code
```javascript
function on(eventName, callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('Callback must be a function');
  }

  var allCallbacks = callbacksFor(this),
      callbacks = undefined;

  callbacks = allCallbacks[eventName];

  if (!callbacks) {
    callbacks = allCallbacks[eventName] = [];
  }

  if (indexOf(callbacks, callback) === -1) {
    callbacks.push(callback);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.setupNodes"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>setupNodes ()](#apidoc.element.broccoli.Builder.prototype.setupNodes)
- description and source-code
```javascript
setupNodes = function () {
  for (var i = 0; i < this.nodeWrappers.length; i++) {
    var nw = this.nodeWrappers[i]
    try {
      nw.setup(this.features)
    } catch (err) {
      throw new NodeSetupError(err, nw)
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.setupTmpDirs"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>setupTmpDirs ()](#apidoc.element.broccoli.Builder.prototype.setupTmpDirs)
- description and source-code
```javascript
setupTmpDirs = function () {
  // Create temporary directories for each node:
  //
  //   out-01-someplugin/
  //   out-02-otherplugin/
  //   cache-01-someplugin/
  //   cache-02-otherplugin/
  //
  // Here's an alternative directory structure we might consider (it's not
  // clear which structure makes debugging easier):
  //
  //   01-someplugin/
  //     out/
  //     cache/
  //     in-1 -> ... // symlink for convenience
  //     in-2 -> ...
  //   02-otherplugin/
  //     ...
  var tmpobj = tmp.dirSync({ prefix: 'broccoli-', unsafeCleanup: true, dir: this.tmpdir })
  this.builderTmpDir = tmpobj.name
  this.builderTmpDirCleanup = tmpobj.removeCallback
  for (var i = 0; i < this.nodeWrappers.length; i++) {
    var nodeWrapper = this.nodeWrappers[i]
    if (nodeWrapper.nodeInfo.nodeType === 'transform') {
      nodeWrapper.inputPaths = nodeWrapper.inputNodeWrappers.map(function(nw) {
        return nw.outputPath
      })
      nodeWrapper.outputPath = this.mkTmpDir(nodeWrapper, 'out')

      if (nodeWrapper.nodeInfo.needsCache) {
        nodeWrapper.cachePath = this.mkTmpDir(nodeWrapper, 'cache')
      }
    } else { // nodeType === 'source'
      // We could name this .sourcePath, but with .outputPath the code is simpler.
      nodeWrapper.outputPath = nodeWrapper.nodeInfo.sourceDirectory
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Builder.prototype.trigger"></a>[function <span class="apidocSignatureSpan">broccoli.Builder.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.Builder.prototype.trigger)
- description and source-code
```javascript
function trigger(eventName, options, label) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      callback = undefined;

  if (callbacks = allCallbacks[eventName]) {
    // Don't cache the callbacks.length since it may grow
    for (var i = 0; i < callbacks.length; i++) {
      callback = callbacks[i];

      callback(options, label);
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Watcher"></a>[module broccoli.Watcher](#apidoc.module.broccoli.Watcher)

#### <a name="apidoc.element.broccoli.Watcher.Watcher"></a>[function <span class="apidocSignatureSpan">broccoli.</span>Watcher (builder, options)](#apidoc.element.broccoli.Watcher.Watcher)
- description and source-code
```javascript
function Watcher(builder, options) {
  this.options = options || {}
  if (this.options.debounce == null) this.options.debounce = 100
  this.builder = builder
  this.watcherAdapter = new WatcherAdapter(this.options.saneOptions)
  this.currentBuild = null
  this._rebuildScheduled = false
  this._ready = false
  this._quitting = false
  this._lifetimeDeferred = null
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.Watcher.prototype"></a>[module broccoli.Watcher.prototype](#apidoc.module.broccoli.Watcher.prototype)

#### <a name="apidoc.element.broccoli.Watcher.prototype._build"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_build ()](#apidoc.element.broccoli.Watcher.prototype._build)
- description and source-code
```javascript
_build = function () {
  var self = this

  logger.debug('buildStart')
  this.trigger('buildStart')
  var buildPromise = self.builder.build()
  // Trigger change/error events. Importantly, if somebody else chains to
  // currentBuild, their callback will come after our events have
  // triggered, because we registered our callback first.
  buildPromise.then(function() {
    logger.debug('buildSuccess')
    self.trigger('buildSuccess')
  }, function(err) {
    logger.debug('buildFailure')
    self.trigger('buildFailure', err)
  })
  return buildPromise
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype._change"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_change ()](#apidoc.element.broccoli.Watcher.prototype._change)
- description and source-code
```javascript
_change = function () {
  var self = this

  if (!this._ready) {
    logger.debug('change', 'ignored: before ready')
    return
  }
  if (this._rebuildScheduled) {
    logger.debug('change', 'ignored: rebuild scheduled already')
    return
  }
  logger.debug('change')
  this._rebuildScheduled = true
  // Wait for current build, and ignore build failure
  RSVP.resolve(this.currentBuild).catch(function() { }).then(function() {
    if (self._quitting) return
    var buildPromise = new RSVP.Promise(function(resolve, reject) {
      logger.debug('debounce')
      self.trigger('debounce')
      setTimeout(resolve, self.options.debounce)
    }).then(function() {
      // Only set _rebuildScheduled to false *after* the setTimeout so that
      // change events during the setTimeout don't trigger a second rebuild
      self._rebuildScheduled = false
      return self._build()
    })
    self.currentBuild = buildPromise
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype._error"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_error (err)](#apidoc.element.broccoli.Watcher.prototype._error)
- description and source-code
```javascript
_error = function (err) {
  var self = this

  logger.debug('error', err)
  if (this._quitting) return
  this._quit().catch(function() { }).then(function() {
    self._lifetimeDeferred.reject(err)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype._quit"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>_quit (err)](#apidoc.element.broccoli.Watcher.prototype._quit)
- description and source-code
```javascript
_quit = function (err) {
  var self = this

  this._quitting = true
  logger.debug('quitStart')

  return RSVP.resolve().then(function() {
    return self.watcherAdapter.quit()
  }).finally(function() {
    // Wait for current build, and ignore build failure
    return RSVP.resolve(self.currentBuild).catch(function() { })
  }).finally(function() {
    logger.debug('quitEnd')
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype.off"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.Watcher.prototype.off)
- description and source-code
```javascript
function off(eventName, callback) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      index = undefined;

  if (!callback) {
    allCallbacks[eventName] = [];
    return;
  }

  callbacks = allCallbacks[eventName];

  index = indexOf(callbacks, callback);

  if (index !== -1) {
    callbacks.splice(index, 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype.on"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.Watcher.prototype.on)
- description and source-code
```javascript
function on(eventName, callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('Callback must be a function');
  }

  var allCallbacks = callbacksFor(this),
      callbacks = undefined;

  callbacks = allCallbacks[eventName];

  if (!callbacks) {
    callbacks = allCallbacks[eventName] = [];
  }

  if (indexOf(callbacks, callback) === -1) {
    callbacks.push(callback);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype.quit"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>quit ()](#apidoc.element.broccoli.Watcher.prototype.quit)
- description and source-code
```javascript
quit = function () {
  var self = this

  if (this._quitting) {
    logger.debug('quit', 'ignored: already quitting')
    return
  }
  this._quit().then(function() {
    self._lifetimeDeferred.resolve()
  }, function(err) {
    self._lifetimeDeferred.reject(err)
  })
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype.start"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>start ()](#apidoc.element.broccoli.Watcher.prototype.start)
- description and source-code
```javascript
start = function () {
  var self = this

  if (this._lifetimeDeferred != null) throw new Error('Watcher.prototype.start() must not be called more than once')
  this._lifetimeDeferred = RSVP.defer()

  this.watcherAdapter.on('change', this._change.bind(this))
  this.watcherAdapter.on('error', this._error.bind(this))
  RSVP.resolve().then(function() {
    return self.watcherAdapter.watch(self.builder.watchedPaths)
  }).then(function() {
    logger.debug('ready')
    self._ready = true
    self.currentBuild = self._build()
  }).catch(function(err) {
    self._error(err)
  })

  return this._lifetimeDeferred.promise
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.Watcher.prototype.trigger"></a>[function <span class="apidocSignatureSpan">broccoli.Watcher.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.Watcher.prototype.trigger)
- description and source-code
```javascript
function trigger(eventName, options, label) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      callback = undefined;

  if (callbacks = allCallbacks[eventName]) {
    // Don't cache the callbacks.length since it may grow
    for (var i = 0; i < callbacks.length; i++) {
      callback = callbacks[i];

      callback(options, label);
    }
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.WatcherAdapter"></a>[module broccoli.WatcherAdapter](#apidoc.module.broccoli.WatcherAdapter)

#### <a name="apidoc.element.broccoli.WatcherAdapter.WatcherAdapter"></a>[function <span class="apidocSignatureSpan">broccoli.</span>WatcherAdapter (options)](#apidoc.element.broccoli.WatcherAdapter.WatcherAdapter)
- description and source-code
```javascript
function WatcherAdapter(options) {
  this.options = options || {}
  this.options.filter = this.options.filter || defaultFilterFunction
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.WatcherAdapter.prototype"></a>[module broccoli.WatcherAdapter.prototype](#apidoc.module.broccoli.WatcherAdapter.prototype)

#### <a name="apidoc.element.broccoli.WatcherAdapter.prototype.off"></a>[function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>off (eventName, callback)](#apidoc.element.broccoli.WatcherAdapter.prototype.off)
- description and source-code
```javascript
function off(eventName, callback) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      index = undefined;

  if (!callback) {
    allCallbacks[eventName] = [];
    return;
  }

  callbacks = allCallbacks[eventName];

  index = indexOf(callbacks, callback);

  if (index !== -1) {
    callbacks.splice(index, 1);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.WatcherAdapter.prototype.on"></a>[function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>on (eventName, callback)](#apidoc.element.broccoli.WatcherAdapter.prototype.on)
- description and source-code
```javascript
function on(eventName, callback) {
  if (typeof callback !== 'function') {
    throw new TypeError('Callback must be a function');
  }

  var allCallbacks = callbacksFor(this),
      callbacks = undefined;

  callbacks = allCallbacks[eventName];

  if (!callbacks) {
    callbacks = allCallbacks[eventName] = [];
  }

  if (indexOf(callbacks, callback) === -1) {
    callbacks.push(callback);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.WatcherAdapter.prototype.quit"></a>[function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>quit ()](#apidoc.element.broccoli.WatcherAdapter.prototype.quit)
- description and source-code
```javascript
quit = function () {
  for (var i = 0; i < this.watchers.length; i++) {
    this.watchers[i].close()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.WatcherAdapter.prototype.trigger"></a>[function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>trigger (eventName, options, label)](#apidoc.element.broccoli.WatcherAdapter.prototype.trigger)
- description and source-code
```javascript
function trigger(eventName, options, label) {
  var allCallbacks = callbacksFor(this),
      callbacks = undefined,
      callback = undefined;

  if (callbacks = allCallbacks[eventName]) {
    // Don't cache the callbacks.length since it may grow
    for (var i = 0; i < callbacks.length; i++) {
      callback = callbacks[i];

      callback(options, label);
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.broccoli.WatcherAdapter.prototype.watch"></a>[function <span class="apidocSignatureSpan">broccoli.WatcherAdapter.prototype.</span>watch (watchedPaths)](#apidoc.element.broccoli.WatcherAdapter.prototype.watch)
- description and source-code
```javascript
watch = function (watchedPaths) {
  var self = this

  this.watchers = []
  this.readyPromises = []
  watchedPaths.forEach(function(watchedPath) {
    var watcher = new sane(watchedPath, self.options)
    function bindFileEvent(event) {
      watcher.on(event, function(filepath, root, stat) {
        logger.debug(event, root + '/' + filepath)
        self.trigger('change')
      })
    }
    bindFileEvent('change')
    bindFileEvent('add')
    bindFileEvent('delete')
    watcher.on('error', function(err) {
      logger.debug('error', err)
      self.trigger('error', err)
    })
    var readyPromise = new RSVP.Promise(function(resolve, reject) {
      watcher.on('ready', function() {
        logger.debug('ready', watchedPath)
        resolve()
      })
    })
    self.watchers.push(watcher)
    self.readyPromises.push(readyPromise)
  })
  return RSVP.Promise.all(this.readyPromises)
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.broccoli.server"></a>[module broccoli.server](#apidoc.module.broccoli.server)

#### <a name="apidoc.element.broccoli.server.serve"></a>[function <span class="apidocSignatureSpan">broccoli.server.</span>serve (watcher, host, port)](#apidoc.element.broccoli.server.serve)
- description and source-code
```javascript
function serve(watcher, host, port) {
  if (watcher.constructor.name !== 'Watcher') throw new Error('Expected Watcher instance')
  if (typeof host !== 'string') throw new Error('Expected host to bind to (e.g. "localhost")')
  if (typeof port !== 'number') throw new Error('Expected port to bind to (e.g. 4200)')

  var server = {}

  console.log('Serving on http://' + host + ':' + port + '\n')

  server.watcher = watcher
  server.builder = server.watcher.builder

  server.app = connect().use(middleware(server.watcher))

  server.http = http.createServer(server.app)

  // We register these so the 'exit' handler removing temp dirs is called
  function cleanupAndExit() {
    return server.watcher.quit()
  }

  process.on('SIGINT', cleanupAndExit)
  process.on('SIGTERM', cleanupAndExit)

  server.watcher.on('buildSuccess', function() {
    printSlowNodes(server.builder.outputNodeWrapper)
    console.log('Built - ' + Math.round(server.builder.outputNodeWrapper.buildState.totalTime) + ' ms @ ' + new Date().toString())
  })

  server.watcher.on('buildFailure', function(err) {
    console.log('Built with error:')
    console.log(err.message)
    if (!err.broccoliPayload || !err.broccoliPayload.location.file) {
      console.log('')
      console.log(err.stack)
    }
    console.log('')
  })

  server.watcher.start()
    .catch(function(err) {
      console.log(err && err.stack || err)
    })
    .finally(function() {
      server.builder.cleanup()
      server.http.close()
    })
    .catch(function(err) {
      console.log('Cleanup error:')
      console.log(err && err.stack || err)
    })
    .finally(function() {
      process.exit(1)
    })

  server.http.listen(parseInt(port, 10), host)
  return server
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
