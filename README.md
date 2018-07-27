# openwhisk-fqn

[![Travis](https://travis-ci.org/ibm-functions/openwhisk-fqn.svg?branch=master)](https://travis-ci.org/ibm-functions/openwhisk-fqn)
[![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Join Slack](https://img.shields.io/badge/join-slack-9B69A0.svg)](http://slack.openwhisk.org/)

Javascript library to convert an [Apache OpenWhisk](https://openwhisk.apache.org) entity name to a fully qualified name.

## Installation

```
npm install openwhisk-fqn
```

## Usage

```javascript
let fqn = require('openwhisk-fqn')

console.log(fqn('action'))                    // outputs '/_/action'
console.log(fqn('package/action'))            // outputs '/_/package/action'
console.log(fqn('/namespace/action'))         // outputs '/namespace/action'
console.log(fqn('/namespace/package/action')) // outputs '/namespace/package/action'
console.log(fqn(null))                        // throws  'Name must be a string'
console.log(fqn('/a/b/c/d'))                  // throws  'Name is not valid'
```
