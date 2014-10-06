# Force Require

[![Build Status](http://img.shields.io/travis/Kikobeats/force-require/master.svg?style=flat)](https://travis-ci.org/Kikobeats/force-require)
[![Dependency status](http://img.shields.io/david/Kikobeats/force-require.svg?style=flat)](https://david-dm.org/Kikobeats/force-require)
[![Dev Dependencies Status](http://img.shields.io/david/dev/Kikobeats/force-require.svg?style=flat)](https://david-dm.org/Kikobeats/force-require#info=devDependencies)
[![NPM Status](http://img.shields.io/npm/dm/force-require.svg?style=flat)](https://www.npmjs.org/package/forcer-equire)
[![Gittip](http://img.shields.io/gittip/Kikobeats.svg?style=flat)](https://www.gittip.com/Kikobeats/)

> Ensure that a NPM dependency is resolved.

## Install

```bash
npm install force-require --save
```

## Usage

First load the library:

```coffee
forceRequire = require 'force-require'
```
Now you can use like `require` command.

## API

### force-require(\<Object>)

Object parameter can be:

* **name**: the name of the dependency to resolve. If is the unique attribute, is not necessary.
* **repository**: You can resolve the dependency using Github repository instead of NPM package.
* **production**: If is necessary to install a dependency, use npm `production` installer
* **scope**: Set the scope. By default the scope is `process.cwd()`

## Examples

```coffee
async = force-require 'async'
async = force-require name:'async'
async = force-require name:'async', repository: 'caolan/async'
async = force-require name:'async', repository: 'caolan/async', production: true
async = force-require name:'async', repository: 'caolan/async', production: true, scope: process.cwd() + '/testApp'
```

## About version parameter

At this moment `version` parameter for fetch different package version is not supported.

When you load a package, the package is in dynamic memory. To load another version of the package can be resolved using [node virtual machine](http://www.davidmclifton.com/2011/08/18/node-js-virtual-machine-vm-usage/) for instance the different version in other scope and return it.


## License

MIT © [Kiko Beats](http://www.kikobeats.com)


