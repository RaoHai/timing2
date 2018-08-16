timing2 [![Build Status](https://travis-ci.com/debug-tips/timing2.svg)](https://travis-ci.com/debug-tips/timing2) [![npm version](https://badge.fury.io/js/timing2.svg)](http://badge.fury.io/js/timing2) [![Coverage Status](https://coveralls.io/repos/github/debug-tips/timing2/badge.svg?branch=master)](https://coveralls.io/github/debug-tips/timing2?branch=master) [![npm downloads](https://img.shields.io/npm/dm/timing2.svg)](https://www.npmjs.com/package/timing2)
------------
⚡️ The state-of-art web performance metrics collector based on [High Resolution Time API](https://www.w3.org/TR/hr-time-2/), with extended performance information that helps you understand how your website loads.

![timing2](https://img.alicdn.com/tfs/TB1C5U8oYArBKNjSZFLXXc_dVXa-1634-762.png)

[visualize your own data](http://jsbin.com/deyaval/6/edit?html,output)

## Usage

**module**

```bash
npm install --save timing2
```

```js
import timing2 from 'timing2';
timing2({ type: 'page' });
```

**standalone**

```html
<script src="https://unpkg.com/timing2@0.2.0/lib/timing2.js"></script>
<script>
  timing2({ type: 'page' });
</script>
```

## API

TODO

## Sample Data

```json
[
  {
    "name": "load",
    "type": "interval",
    "time": 2800.8999999728985
  },
  {
    "name": "domContentLoaded",
    "type": "interval",
    "time": 2094.2999999970198
  },
  {
    "name": "timeToFirstByte",
    "type": "interval",
    "time": 1369.6999999810942
  },
  {
    "name": "firstPaint",
    "type": "interval",
    "time": 1795.0999999884516
  },
  {
    "name": "firstContentfulPaint",
    "type": "interval",
    "time": 1795.0999999884516
  },
  {
    "name": "redirect",
    "type": "duration",
    "time": 0,
    "durationType": "networking"
  },
  {
    "name": "appcache",
    "type": "duration",
    "time": 0,
    "durationType": "networking"
  },
  {
    "name": "dnsLookup",
    "type": "duration",
    "time": 0,
    "durationType": "networking"
  },
  {
    "name": "stalled",
    "type": "duration",
    "time": 7.999999972525984,
    "durationType": "networking"
  },
  {
    "name": "connect",
    "type": "duration",
    "time": 247.80000001192093,
    "durationType": "networking"
  },
  {
    "name": "ssl",
    "type": "duration",
    "time": 245.40000001434237,
    "durationType": "networking"
  },
  {
    "name": "request",
    "type": "duration",
    "time": 1079.3999999877997,
    "durationType": "server"
  },
  {
    "name": "response",
    "type": "duration",
    "time": 327.69999996526167,
    "durationType": "server"
  },
  {
    "name": "parseHTML",
    "type": "duration",
    "time": 396.90000005066395,
    "durationType": "client"
  },
  {
    "name": "loadCritialResources",
    "type": "duration",
    "time": 396.90000005066395,
    "durationType": "client"
  },
  {
    "name": "loadAllResources",
    "type": "duration",
    "time": 1094.9000000255182,
    "durationType": "client"
  },
  {
    "name": "domReadyEvent",
    "type": "duration",
    "time": 106.70000000391155,
    "durationType": "client"
  },
  {
    "name": "loadEvent",
    "type": "duration",
    "time": 8.600000001024455,
    "durationType": "client"
  }
]
```

## ChangeLog

### v0.1.0
- Add page metrics

### v0.2.0
- Refactor to split modules
- Add `unloadEvent`
- Add `unpkg` support

## Prior Art

- [timing.js](https://github.com/addyosmani/timing.js)
- [lighthouse](https://github.com/GoogleChrome/lighthouse)
