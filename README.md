# WeDeploy SDK for JavaScript
[![Build Status][build-status-svg]][build-status-link]
[![Test Coverage][coverage-status-svg]][coverage-status-link]
[![License][license-svg]][license-link]
[![Npm Version][npm-svg]][npm-link]

[![Build Status](https://saucelabs.com/browser-matrix/ivansantos.svg)](https://saucelabs.com/beta/builds/8a24c731fc704e2c835033bcbc2faa2e)

An SDK that gives you access to the powerful WeDeploy cloud platforma from your JavaScript app. For more information on WeDeploy and its features, see [the website](https://wedeploy.com) or [the JavaScript guide](https://wedeploy.com/docs).

## Getting Started

The easiest way to integrate the WeDeploy SDK into your JavaScript project is through the [npm module](https://npmjs.org/wedeploy) or you can fetch it from our [CDN](http://cdn.wedeploy.com/api/latest/wedeploy.js).

## Usage

Post

```javascript
WeDeploy
  .url('/data/tasks')
  .post({ desc: 'Buy milk' });
```

Get

```javascript
WeDeploy
	.url('/data/tasks')
	.get()
	.then(function(clientResponse) {
	  console.log(clientResponse.body());
	});
```

Data

```javascript
WeDeploy
	.data('http://mydata.dataproject.wedeploy.io')
	.get('movies')
	.then(function(movies) {
	  console.log(movies);
	});
```

## Setup

```
npm install
```

## Build

```
gulp build
```

```
gulp watch
```

## Test

### Test on node.js

```
gulp test:node
```


### Test on browsers

```
gulp test
```

```
gulp test:watch
```

## License

```
Copyright (c) 2016-present, Liferay Inc
All rights reserved.

This source code is licensed under the BSD-style license found in the
LICENSE file in the root directory of this source tree. An additional grant 
of patent rights can be found in the PATENTS file in the same directory.
```


[build-status-svg]: https://travis-ci.com/wedeploy/api-js.svg?token=a51FNuiJPYZtHhup9q1V&branch=master
[build-status-link]: https://travis-ci.com/wedeploy/api-js


[coverage-status-svg]: http://codecov.io/github/wedeploy/api-js/coverage.svg?branch=master
[coverage-status-link]: http://codecov.io/github/wedeploy/api-js?branch=master

[license-svg]: https://img.shields.io/badge/license-BSD-lightgrey.svg
[license-link]: https://github.com/wedeploy/api-js/blob/master/LICENSE.md

[npm-svg]: https://badge.fury.io/js/wedeploy.svg
[npm-link]: https://npmjs.org/wedeploy
