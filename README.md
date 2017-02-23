# SyncWriteStream from Node.js Core

The `fs.SyncWriteStream` class in Node.js core was always meant to be used
by Node.js core itself and was never documented as a publicly supported API.
In Node.js 6.0.0 it was deprecated in docs, and in Node.js 8.0.0 a runtime
deprecation warning will be issued when `fs.SyncWriteStream` is used.

This module may be used as a drop in replacement in the off chance userland
code was written to depend on `fs.SyncWriteStream`.

The implementation is a straightforward copy of the Node.js core implementation.

```js
const SyncWriteStream = require('syncwritestream');

const str = new SyncWriteStream();
```

