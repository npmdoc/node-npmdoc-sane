# api documentation for  [sane (v1.6.0)](https://github.com/amasad/sane)  [![npm package](https://img.shields.io/npm/v/npmdoc-sane.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-sane) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-sane.svg)](https://travis-ci.org/npmdoc/node-npmdoc-sane)
#### Sane aims to be fast, small, and reliable file system watcher.

[![NPM](https://nodei.co/npm/sane.png?downloads=true)](https://www.npmjs.com/package/sane)

[![apidoc](https://npmdoc.github.io/node-npmdoc-sane/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-sane_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-sane/build/apidoc.html)

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
            "name": "amasad",
            "email": "amjad.masad@gmail.com"
        },
        {
            "name": "stefanpenner",
            "email": "stefan.penner@gmail.com"
        }
    ],
    "name": "sane",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module sane](#apidoc.module.sane)
1.  [function <span class="apidocSignatureSpan">sane.</span>NodeWatcher (dir, opts)](#apidoc.element.sane.NodeWatcher)
1.  [function <span class="apidocSignatureSpan">sane.</span>PollWatcher (dir, opts)](#apidoc.element.sane.PollWatcher)
1.  [function <span class="apidocSignatureSpan">sane.</span>WatchmanWatcher (dir, opts)](#apidoc.element.sane.WatchmanWatcher)
1.  object <span class="apidocSignatureSpan">sane.</span>NodeWatcher.prototype
1.  object <span class="apidocSignatureSpan">sane.</span>PollWatcher.prototype
1.  object <span class="apidocSignatureSpan">sane.</span>WatchmanWatcher.prototype
1.  object <span class="apidocSignatureSpan">sane.</span>common

#### [module sane.NodeWatcher](#apidoc.module.sane.NodeWatcher)
1.  [function <span class="apidocSignatureSpan">sane.</span>NodeWatcher (dir, opts)](#apidoc.element.sane.NodeWatcher.NodeWatcher)

#### [module sane.NodeWatcher.prototype](#apidoc.module.sane.NodeWatcher.prototype)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>close (callback)](#apidoc.element.sane.NodeWatcher.prototype.close)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>detectChangedFile (dir, event, callback)](#apidoc.element.sane.NodeWatcher.prototype.detectChangedFile)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>emitEvent (type, file, stat)](#apidoc.element.sane.NodeWatcher.prototype.emitEvent)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>normalizeChange (dir, event, file)](#apidoc.element.sane.NodeWatcher.prototype.normalizeChange)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>processChange (dir, event, file)](#apidoc.element.sane.NodeWatcher.prototype.processChange)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>register (filepath)](#apidoc.element.sane.NodeWatcher.prototype.register)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>registered (fullpath)](#apidoc.element.sane.NodeWatcher.prototype.registered)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>stopWatching (dir)](#apidoc.element.sane.NodeWatcher.prototype.stopWatching)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>unregister (filepath)](#apidoc.element.sane.NodeWatcher.prototype.unregister)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>unregisterDir (dirpath)](#apidoc.element.sane.NodeWatcher.prototype.unregisterDir)
1.  [function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>watchdir (dir)](#apidoc.element.sane.NodeWatcher.prototype.watchdir)

#### [module sane.PollWatcher](#apidoc.module.sane.PollWatcher)
1.  [function <span class="apidocSignatureSpan">sane.</span>PollWatcher (dir, opts)](#apidoc.element.sane.PollWatcher.PollWatcher)

#### [module sane.PollWatcher.prototype](#apidoc.module.sane.PollWatcher.prototype)
1.  [function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>close (callback)](#apidoc.element.sane.PollWatcher.prototype.close)
1.  [function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>emitEvent (type, file, stat)](#apidoc.element.sane.PollWatcher.prototype.emitEvent)
1.  [function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>filter (filepath, stat)](#apidoc.element.sane.PollWatcher.prototype.filter)
1.  [function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>init (monitor)](#apidoc.element.sane.PollWatcher.prototype.init)

#### [module sane.WatchmanWatcher](#apidoc.module.sane.WatchmanWatcher)
1.  [function <span class="apidocSignatureSpan">sane.</span>WatchmanWatcher (dir, opts)](#apidoc.element.sane.WatchmanWatcher.WatchmanWatcher)

#### [module sane.WatchmanWatcher.prototype](#apidoc.module.sane.WatchmanWatcher.prototype)
1.  [function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>close (callback)](#apidoc.element.sane.WatchmanWatcher.prototype.close)
1.  [function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>emitEvent ( eventType, filepath, root, stat )](#apidoc.element.sane.WatchmanWatcher.prototype.emitEvent)
1.  [function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>handleChangeEvent (resp)](#apidoc.element.sane.WatchmanWatcher.prototype.handleChangeEvent)
1.  [function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>handleFileChange (changeDescriptor)](#apidoc.element.sane.WatchmanWatcher.prototype.handleFileChange)
1.  [function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>init ()](#apidoc.element.sane.WatchmanWatcher.prototype.init)

#### [module sane.common](#apidoc.module.sane.common)
1.  [function <span class="apidocSignatureSpan">sane.common.</span>assignOptions (watcher, opts)](#apidoc.element.sane.common.assignOptions)
1.  [function <span class="apidocSignatureSpan">sane.common.</span>isFileIncluded (globs, dot, doIgnore, relativePath)](#apidoc.element.sane.common.isFileIncluded)
1.  number <span class="apidocSignatureSpan">sane.common.</span>DEFAULT_DELAY
1.  string <span class="apidocSignatureSpan">sane.common.</span>ADD_EVENT
1.  string <span class="apidocSignatureSpan">sane.common.</span>ALL_EVENT
1.  string <span class="apidocSignatureSpan">sane.common.</span>CHANGE_EVENT
1.  string <span class="apidocSignatureSpan">sane.common.</span>DELETE_EVENT



# <a name="apidoc.module.sane"></a>[module sane](#apidoc.module.sane)

#### <a name="apidoc.element.sane.NodeWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>NodeWatcher (dir, opts)](#apidoc.element.sane.NodeWatcher)
- description and source-code
```javascript
function NodeWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);

  this.watched = Object.create(null);
  this.changeTimers = Object.create(null);
  this.dirRegistery = Object.create(null);
  this.root = path.resolve(dir);
  this.watchdir = this.watchdir.bind(this);
  this.register = this.register.bind(this);

  this.watchdir(this.root);
  recReaddir(
    this.root,
    this.watchdir,
    this.register,
    this.emit.bind(this, 'ready'),
    this.ignored
  );
}
```
- example usage
```shell
...
* 'dot': enables watching files/directories that start with a dot.
* 'ignored': a glob, regex, function, or array of any combination.

For the glob pattern documentation, see [minimatch](https://github.com/isaacs/minimatch).
If you choose to use 'watchman' you'll have to [install watchman yourself](https://facebook.github.io/watchman/docs/install.html
)).
For the ignored options, see [anymatch](https://github.com/es128/anymatch).

### sane.NodeWatcher(dir, options)

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.
...
```

#### <a name="apidoc.element.sane.PollWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>PollWatcher (dir, opts)](#apidoc.element.sane.PollWatcher)
- description and source-code
```javascript
function PollWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);

  this.watched = Object.create(null);
  this.root = path.resolve(dir);

  watch.createMonitor(
    this.root,
    { interval: opts.interval || DEFAULT_DELAY,
      filter: this.filter.bind(this)
    },
    this.init.bind(this)
  );
}
```
- example usage
```shell
...

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.

### sane.PollWatcher(dir, options)

The polling watcher class. Takes the same options as 'sane(options, dir)' with the addition of:

* interval: indicates how often the files should be polled. (passed to fs.watchFile)

### sane.{Node|Watchman|Poll}Watcher#close
...
```

#### <a name="apidoc.element.sane.WatchmanWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>WatchmanWatcher (dir, opts)](#apidoc.element.sane.WatchmanWatcher)
- description and source-code
```javascript
function WatchmanWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);
  this.root = path.resolve(dir);
  this.init();
}
```
- example usage
```shell
...
If you choose to use 'watchman' you'll have to [install watchman yourself](https://facebook.github.io/watchman/docs/install.html
)).
For the ignored options, see [anymatch](https://github.com/es128/anymatch).

### sane.NodeWatcher(dir, options)

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.

### sane.PollWatcher(dir, options)

The polling watcher class. Takes the same options as 'sane(options, dir)' with the addition of:
...
```



# <a name="apidoc.module.sane.NodeWatcher"></a>[module sane.NodeWatcher](#apidoc.module.sane.NodeWatcher)

#### <a name="apidoc.element.sane.NodeWatcher.NodeWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>NodeWatcher (dir, opts)](#apidoc.element.sane.NodeWatcher.NodeWatcher)
- description and source-code
```javascript
function NodeWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);

  this.watched = Object.create(null);
  this.changeTimers = Object.create(null);
  this.dirRegistery = Object.create(null);
  this.root = path.resolve(dir);
  this.watchdir = this.watchdir.bind(this);
  this.register = this.register.bind(this);

  this.watchdir(this.root);
  recReaddir(
    this.root,
    this.watchdir,
    this.register,
    this.emit.bind(this, 'ready'),
    this.ignored
  );
}
```
- example usage
```shell
...
* 'dot': enables watching files/directories that start with a dot.
* 'ignored': a glob, regex, function, or array of any combination.

For the glob pattern documentation, see [minimatch](https://github.com/isaacs/minimatch).
If you choose to use 'watchman' you'll have to [install watchman yourself](https://facebook.github.io/watchman/docs/install.html
)).
For the ignored options, see [anymatch](https://github.com/es128/anymatch).

### sane.NodeWatcher(dir, options)

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.
...
```



# <a name="apidoc.module.sane.NodeWatcher.prototype"></a>[module sane.NodeWatcher.prototype](#apidoc.module.sane.NodeWatcher.prototype)

#### <a name="apidoc.element.sane.NodeWatcher.prototype.close"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>close (callback)](#apidoc.element.sane.NodeWatcher.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  Object.keys(this.watched).forEach(this.stopWatching, this);
  this.removeAllListeners();
  if (typeof callback === 'function') {
    setImmediate(callback.bind(null, null, true));
  }
}
```
- example usage
```shell
...
'''js
var watcher = sane('path/to/dir', {glob: ['**/*.js', '**/*.css']});
watcher.on('ready', function () { console.log('ready') });
watcher.on('change', function (filepath, root, stat) { console.log('file changed', filepath); });
watcher.on('add', function (filepath, root, stat) { console.log('file added', filepath); });
watcher.on('delete', function (filepath, root) { console.log('file deleted', filepath); });
// close
watcher.close();
'''

options:

* 'glob': a single string glob pattern or an array of them.
* 'poll': puts the watcher in polling mode. Under the hood that means 'fs.watchFile'.
* 'watchman': makes the watcher use [watchman](https://facebook.github.io/watchman/).
...
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.detectChangedFile"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>detectChangedFile (dir, event, callback)](#apidoc.element.sane.NodeWatcher.prototype.detectChangedFile)
- description and source-code
```javascript
detectChangedFile = function (dir, event, callback) {
  if (!this.dirRegistery[dir]) {
    return;
  }

  var found = false;
  var closest = {mtime: 0};
  var c = 0;
  Object.keys(this.dirRegistery[dir]).forEach(function(file, i, arr) {
    fs.lstat(path.join(dir, file), function(error, stat) {
      if (found) {
        return;
      }

      if (error) {
        if (error.code === 'ENOENT' ||
            (platform === 'win32' && error.code === 'EPERM')) {
          found = true;
          callback(file);
        } else {
          this.emit('error', error);
        }
      } else {
        if (stat.mtime > closest.mtime) {
          stat.file = file;
          closest = stat;
        }
        if (arr.length === ++c) {
          callback(closest.file);
        }
      }
    }.bind(this));
  }, this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.emitEvent"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>emitEvent (type, file, stat)](#apidoc.element.sane.NodeWatcher.prototype.emitEvent)
- description and source-code
```javascript
emitEvent = function (type, file, stat) {
  var key = type + '-' + file;
  var addKey = ADD_EVENT + '-' + file;
  if (type === CHANGE_EVENT && this.changeTimers[addKey]) {
    // Ignore the change event that is immediately fired after an add event.
    // (This happens on Linux).
    return;
  }
  clearTimeout(this.changeTimers[key]);
  this.changeTimers[key] = setTimeout(function() {
    delete this.changeTimers[key];
    this.emit(type, file, this.root, stat);
    this.emit(ALL_EVENT, type, file, this.root, stat);
  }.bind(this), DEFAULT_DELAY);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.normalizeChange"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>normalizeChange (dir, event, file)](#apidoc.element.sane.NodeWatcher.prototype.normalizeChange)
- description and source-code
```javascript
normalizeChange = function (dir, event, file) {
  if (!file) {
    this.detectChangedFile(dir, event, function(actualFile) {
      if (actualFile) {
        this.processChange(dir, event, actualFile);
      }
    }.bind(this));
  } else {
    this.processChange(dir, event, path.normalize(file));
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.processChange"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>processChange (dir, event, file)](#apidoc.element.sane.NodeWatcher.prototype.processChange)
- description and source-code
```javascript
processChange = function (dir, event, file) {
  var fullPath = path.join(dir, file);
  var relativePath = path.join(path.relative(this.root, dir), file);
  fs.lstat(fullPath, function(error, stat) {
    if (error && error.code !== 'ENOENT') {
      this.emit('error', error);
    } else if (!error && stat.isDirectory()) {
      // win32 emits usless change events on dirs.
      if (event !== 'change') {
        this.watchdir(fullPath);
        if (common.isFileIncluded(
          this.globs,
          this.dot,
          this.doIgnore,
          relativePath)) {
          this.emitEvent(ADD_EVENT, relativePath, stat);
        }
      }
    } else {
      var registered = this.registered(fullPath);
      if (error && error.code === 'ENOENT') {
        this.unregister(fullPath);
        this.stopWatching(fullPath);
        this.unregisterDir(fullPath);
        if (registered) {
          this.emitEvent(DELETE_EVENT, relativePath);
        }
      } else if (registered) {
        this.emitEvent(CHANGE_EVENT, relativePath, stat);
      } else {
        if (this.register(fullPath)) {
          this.emitEvent(ADD_EVENT, relativePath, stat);
        }
      }
    }
  }.bind(this));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.register"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>register (filepath)](#apidoc.element.sane.NodeWatcher.prototype.register)
- description and source-code
```javascript
register = function (filepath) {
  var relativePath = path.relative(this.root, filepath);
  if (!common.isFileIncluded(
    this.globs,
    this.dot,
    this.doIgnore,
    relativePath)) {
    return false;
  }

  var dir = path.dirname(filepath);
  if (!this.dirRegistery[dir]) {
    this.dirRegistery[dir] = Object.create(null);
  }

  var filename = path.basename(filepath);
  this.dirRegistery[dir][filename] = true;

  return true;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.registered"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>registered (fullpath)](#apidoc.element.sane.NodeWatcher.prototype.registered)
- description and source-code
```javascript
registered = function (fullpath) {
  var dir = path.dirname(fullpath);
  return this.dirRegistery[fullpath] ||
    this.dirRegistery[dir] && this.dirRegistery[dir][path.basename(fullpath)];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.stopWatching"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>stopWatching (dir)](#apidoc.element.sane.NodeWatcher.prototype.stopWatching)
- description and source-code
```javascript
stopWatching = function (dir) {
  if (this.watched[dir]) {
    this.watched[dir].close();
    delete this.watched[dir];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.unregister"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>unregister (filepath)](#apidoc.element.sane.NodeWatcher.prototype.unregister)
- description and source-code
```javascript
unregister = function (filepath) {
  var dir = path.dirname(filepath);
  if (this.dirRegistery[dir]) {
    var filename = path.basename(filepath);
    delete this.dirRegistery[dir][filename];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.unregisterDir"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>unregisterDir (dirpath)](#apidoc.element.sane.NodeWatcher.prototype.unregisterDir)
- description and source-code
```javascript
unregisterDir = function (dirpath) {
  if (this.dirRegistery[dirpath]) {
    delete this.dirRegistery[dirpath];
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.NodeWatcher.prototype.watchdir"></a>[function <span class="apidocSignatureSpan">sane.NodeWatcher.prototype.</span>watchdir (dir)](#apidoc.element.sane.NodeWatcher.prototype.watchdir)
- description and source-code
```javascript
watchdir = function (dir) {
  if (this.watched[dir]) {
    return;
  }

  var watcher = fs.watch(
    dir,
    { persistent: true },
    this.normalizeChange.bind(this, dir)
  );
  this.watched[dir] = watcher;

  // Workaround Windows node issue #4337.
  if (platform === 'win32') {
    watcher.on('error', function(error) {
      if (error.code !== 'EPERM') {
        throw error;
      }
    });
  }

  if (this.root !== dir) {
    this.register(dir);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sane.PollWatcher"></a>[module sane.PollWatcher](#apidoc.module.sane.PollWatcher)

#### <a name="apidoc.element.sane.PollWatcher.PollWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>PollWatcher (dir, opts)](#apidoc.element.sane.PollWatcher.PollWatcher)
- description and source-code
```javascript
function PollWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);

  this.watched = Object.create(null);
  this.root = path.resolve(dir);

  watch.createMonitor(
    this.root,
    { interval: opts.interval || DEFAULT_DELAY,
      filter: this.filter.bind(this)
    },
    this.init.bind(this)
  );
}
```
- example usage
```shell
...

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.

### sane.PollWatcher(dir, options)

The polling watcher class. Takes the same options as 'sane(options, dir)' with the addition of:

* interval: indicates how often the files should be polled. (passed to fs.watchFile)

### sane.{Node|Watchman|Poll}Watcher#close
...
```



# <a name="apidoc.module.sane.PollWatcher.prototype"></a>[module sane.PollWatcher.prototype](#apidoc.module.sane.PollWatcher.prototype)

#### <a name="apidoc.element.sane.PollWatcher.prototype.close"></a>[function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>close (callback)](#apidoc.element.sane.PollWatcher.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  Object.keys(this.watched).forEach(function(filepath) {
    fs.unwatchFile(filepath);
  });
  this.removeAllListeners();
  if (typeof callback === 'function') {
    setImmediate(callback.bind(null, null, true));
  }
}
```
- example usage
```shell
...
'''js
var watcher = sane('path/to/dir', {glob: ['**/*.js', '**/*.css']});
watcher.on('ready', function () { console.log('ready') });
watcher.on('change', function (filepath, root, stat) { console.log('file changed', filepath); });
watcher.on('add', function (filepath, root, stat) { console.log('file added', filepath); });
watcher.on('delete', function (filepath, root) { console.log('file deleted', filepath); });
// close
watcher.close();
'''

options:

* 'glob': a single string glob pattern or an array of them.
* 'poll': puts the watcher in polling mode. Under the hood that means 'fs.watchFile'.
* 'watchman': makes the watcher use [watchman](https://facebook.github.io/watchman/).
...
```

#### <a name="apidoc.element.sane.PollWatcher.prototype.emitEvent"></a>[function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>emitEvent (type, file, stat)](#apidoc.element.sane.PollWatcher.prototype.emitEvent)
- description and source-code
```javascript
emitEvent = function (type, file, stat) {
  file = path.relative(this.root, file);

  if (type === DELETE_EVENT) {
    // Matching the non-polling API
    stat = null;
  }

  this.emit(type, file, this.root, stat);
  this.emit(ALL_EVENT, type, file, this.root, stat);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.PollWatcher.prototype.filter"></a>[function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>filter (filepath, stat)](#apidoc.element.sane.PollWatcher.prototype.filter)
- description and source-code
```javascript
filter = function (filepath, stat) {
  return stat.isDirectory() || common.isFileIncluded(
    this.globs,
    this.dot,
    this.doIgnore,
    path.relative(this.root, filepath)
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.PollWatcher.prototype.init"></a>[function <span class="apidocSignatureSpan">sane.PollWatcher.prototype.</span>init (monitor)](#apidoc.element.sane.PollWatcher.prototype.init)
- description and source-code
```javascript
init = function (monitor) {
  this.watched = monitor.files;
  monitor.on('changed', this.emitEvent.bind(this, CHANGE_EVENT));
  monitor.on('removed', this.emitEvent.bind(this, DELETE_EVENT));
  monitor.on('created', this.emitEvent.bind(this, ADD_EVENT));
  // 1 second wait because mtime is second-based.
  setTimeout(this.emit.bind(this, 'ready'), 1000);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sane.WatchmanWatcher"></a>[module sane.WatchmanWatcher](#apidoc.module.sane.WatchmanWatcher)

#### <a name="apidoc.element.sane.WatchmanWatcher.WatchmanWatcher"></a>[function <span class="apidocSignatureSpan">sane.</span>WatchmanWatcher (dir, opts)](#apidoc.element.sane.WatchmanWatcher.WatchmanWatcher)
- description and source-code
```javascript
function WatchmanWatcher(dir, opts) {
  opts = common.assignOptions(this, opts);
  this.root = path.resolve(dir);
  this.init();
}
```
- example usage
```shell
...
If you choose to use 'watchman' you'll have to [install watchman yourself](https://facebook.github.io/watchman/docs/install.html
)).
For the ignored options, see [anymatch](https://github.com/es128/anymatch).

### sane.NodeWatcher(dir, options)

The default watcher class. Uses 'fs.watch' under the hood, and takes the same options as 'sane(options, dir)'.

### sane.WatchmanWatcher(dir, options)

The watchman watcher class. Takes the same options as 'sane(options, dir)'.

### sane.PollWatcher(dir, options)

The polling watcher class. Takes the same options as 'sane(options, dir)' with the addition of:
...
```



# <a name="apidoc.module.sane.WatchmanWatcher.prototype"></a>[module sane.WatchmanWatcher.prototype](#apidoc.module.sane.WatchmanWatcher.prototype)

#### <a name="apidoc.element.sane.WatchmanWatcher.prototype.close"></a>[function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>close (callback)](#apidoc.element.sane.WatchmanWatcher.prototype.close)
- description and source-code
```javascript
close = function (callback) {
  this.client.removeAllListeners();
  this.client.end();
  callback && callback(null, true);
}
```
- example usage
```shell
...
'''js
var watcher = sane('path/to/dir', {glob: ['**/*.js', '**/*.css']});
watcher.on('ready', function () { console.log('ready') });
watcher.on('change', function (filepath, root, stat) { console.log('file changed', filepath); });
watcher.on('add', function (filepath, root, stat) { console.log('file added', filepath); });
watcher.on('delete', function (filepath, root) { console.log('file deleted', filepath); });
// close
watcher.close();
'''

options:

* 'glob': a single string glob pattern or an array of them.
* 'poll': puts the watcher in polling mode. Under the hood that means 'fs.watchFile'.
* 'watchman': makes the watcher use [watchman](https://facebook.github.io/watchman/).
...
```

#### <a name="apidoc.element.sane.WatchmanWatcher.prototype.emitEvent"></a>[function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>emitEvent ( eventType, filepath, root, stat )](#apidoc.element.sane.WatchmanWatcher.prototype.emitEvent)
- description and source-code
```javascript
emitEvent = function ( eventType, filepath, root, stat ) {
  this.emit(eventType, filepath, root, stat);
  this.emit(ALL_EVENT, eventType, filepath, root, stat);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.WatchmanWatcher.prototype.handleChangeEvent"></a>[function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>handleChangeEvent (resp)](#apidoc.element.sane.WatchmanWatcher.prototype.handleChangeEvent)
- description and source-code
```javascript
handleChangeEvent = function (resp) {
  assert.equal(resp.subscription, SUB_NAME, 'Invalid subscription event.');
  if (Array.isArray(resp.files)) {
    resp.files.forEach(this.handleFileChange, this);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.WatchmanWatcher.prototype.handleFileChange"></a>[function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>handleFileChange (changeDescriptor)](#apidoc.element.sane.WatchmanWatcher.prototype.handleFileChange)
- description and source-code
```javascript
handleFileChange = function (changeDescriptor) {
  var self = this;
  var absPath;
  var relativePath;

  if (this.capabilities.relative_root) {
    relativePath = changeDescriptor.name;
    absPath = path.join(
      this.watchProjectInfo.root,
      this.watchProjectInfo.relativePath,
      relativePath
    );
  } else {
    absPath = path.join(this.root, changeDescriptor.name);
    relativePath = changeDescriptor.name;
  }

  if (!(self.capabilities.wildmatch && !this.hasIgnore) &&
      !common.isFileIncluded(
        this.globs,
        this.dot,
        this.doIgnore,
        relativePath)) {
    return;
  }

  if (!changeDescriptor.exists) {
    self.emitEvent(DELETE_EVENT, relativePath, self.root);
  } else {
    fs.lstat(absPath, function(error, stat) {
      // Files can be deleted between the event and the lstat call
      // the most reliable thing to do here is to ignore the event.
      if (error && error.code === 'ENOENT') {
        return;
      }

      if (handleError(self, error)) {
        return;
      }

      var eventType = changeDescriptor.new ? ADD_EVENT : CHANGE_EVENT;

      // Change event on dirs are mostly useless.
      if (!(eventType === CHANGE_EVENT && stat.isDirectory())) {
        self.emitEvent(eventType, relativePath, self.root, stat);
      }
    });
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.WatchmanWatcher.prototype.init"></a>[function <span class="apidocSignatureSpan">sane.WatchmanWatcher.prototype.</span>init ()](#apidoc.element.sane.WatchmanWatcher.prototype.init)
- description and source-code
```javascript
init = function () {
  if (this.client) {
    this.client.removeAllListeners();
  }

  var self = this;
  this.client = new watchman.Client();
  this.client.on('error', function(error) {
    self.emit('error', error);
  });
  this.client.on('subscription', this.handleChangeEvent.bind(this));
  this.client.on('end', function() {
    console.warn('[sane] Warning: Lost connection to watchman, reconnecting..');
    self.init();
  });

  this.watchProjectInfo = null;

  function getWatchRoot() {
    return self.watchProjectInfo ? self.watchProjectInfo.root : self.root;
  }

  function onCapability(error, resp) {
    if (handleError(self, error)) {
      // The Watchman watcher is unusable on this system, we cannot continue
      return;
    }

    handleWarning(resp);

    self.capabilities = resp.capabilities;

    if (self.capabilities.relative_root) {
      self.client.command(
        ['watch-project', getWatchRoot()], onWatchProject
      );
    } else {
      self.client.command(['watch', getWatchRoot()], onWatch);
    }
  }

  function onWatchProject(error, resp) {
    if (handleError(self, error)) {
      return;
    }

    handleWarning(resp);

    self.watchProjectInfo = {
      root: resp.watch,
      relativePath: resp.relative_path ? resp.relative_path : ''
    };

    self.client.command(['clock', getWatchRoot()], onClock);
  }


  function onWatch(error, resp) {
    if (handleError(self, error)) {
      return;
    }

    handleWarning(resp);

    self.client.command(['clock', getWatchRoot()], onClock);
  }

  function onClock(error, resp) {
    if (handleError(self, error)) {
      return;
    }

    handleWarning(resp);

    var options = {
      fields: ['name', 'exists', 'new'],
      since: resp.clock
    };

    // If the server has the wildmatch capability available it supports
    // the recursive **/*.foo style match and we can offload our globs
    // to the watchman server.  This saves both on data size to be
    // communicated back to us and compute for evaluating the globs
    // in our node process.
    if (self.capabilities.wildmatch) {
      if (self.globs.length === 0) {
        if (!self.dot) {
          // Make sure we honor the dot option if even we're not using globs.
          options.expression = ['match', '**', 'wholename', {
            includedotfiles: false
          }];
        }
      } else {
        options.expression = ['anyof'];
        for (var i in self.globs) {
          options.expression.push(['match', self.globs[i], 'wholename', {
            includedotfiles: self.dot
          }]);
        }
      }
    }

    if (self.capabilities.relative_root) {
      options.relative_root = self.watchProjectInfo.relativePath;
    }

    self.client.command(
      ['subscribe', getWatchRoot(), SUB_NAME, options],
      onSubscribe
    );
  }

  function onSubscribe(error, resp) {
    if (handleError(self, error)) {
      return;
    }

    handleWarning(resp);

    self.emit('ready');
  }

  self.client.capabilityCheck({
      optional:['wildmatch', 'relative_root']
    },
    onCapability);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.sane.common"></a>[module sane.common](#apidoc.module.sane.common)

#### <a name="apidoc.element.sane.common.assignOptions"></a>[function <span class="apidocSignatureSpan">sane.common.</span>assignOptions (watcher, opts)](#apidoc.element.sane.common.assignOptions)
- description and source-code
```javascript
assignOptions = function (watcher, opts) {
  opts = opts || {};
  watcher.globs = opts.glob || [];
  watcher.dot = opts.dot || false;
  watcher.ignored = opts.ignored || false;

  if (!Array.isArray(watcher.globs)) {
    watcher.globs = [watcher.globs];
  }
  watcher.hasIgnore = Boolean(opts.ignored) &&
    !(Array.isArray(opts) && opts.length > 0);
  watcher.doIgnore = opts.ignored ? anymatch(opts.ignored) : function () {
    return false;
  };
  return opts;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.sane.common.isFileIncluded"></a>[function <span class="apidocSignatureSpan">sane.common.</span>isFileIncluded (globs, dot, doIgnore, relativePath)](#apidoc.element.sane.common.isFileIncluded)
- description and source-code
```javascript
isFileIncluded = function (globs, dot, doIgnore, relativePath) {
  var matched;
  if (globs.length) {
    for (var i = 0; i < globs.length; i++) {
      if (minimatch(relativePath, globs[i], {dot: dot}) &&
        !doIgnore(relativePath)) {
        matched = true;
        break;
      }
    }
  } else {
    // Make sure we honor the dot option if even we're not using globs.
    matched = (dot || minimatch(relativePath, '**/*')) &&
      !doIgnore(relativePath);
  }
  return matched;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
