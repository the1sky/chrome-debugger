# Chrome Debugger
This is an interface that talks [Chrome's Remote Debugging Protocol](https://developers.google.com/chrome-developer-tools/docs/debugger-protocol).

## Usage
```javascript
var cd = require('chrome-debugger')('ws://localhost:9222/devtools/page/123')
cd.runtime.evaluate('5', console.log.bind(console));
// 5
```

## API

* `require('chrome-debugger')` - This returns a function that given a websocket endpoint for chrome, will return an object that can talk the debugger protocol.

    * 'runtime' - The [runtime](https://developers.google.com/chrome-developer-tools/docs/protocol/1.0/runtime)
        * `evaluate` - (expression, [, callback]), [evaluates](https://developers.google.com/chrome-developer-tools/docs/protocol/1.0/runtime#command-evaluate) the expression on the page.

## Developing
```sh
npm install
```

Afterwards, you can start developing on this.

## LICENSE
[MIT](http://gkatsev.mit-license.org/)
