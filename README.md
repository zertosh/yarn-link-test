Repro steps
===========

* Build yarn with https://github.com/yarnpkg/yarn/pull/3359 and run:

```
$ cd pkg-a
$ yarn
$ node index.js
module.js:472
    throw err;
    ^

Error: Cannot find module 'react'
    at Function.Module._resolveFilename (module.js:470:15)
    at Function.Module._load (module.js:418:25)
    at Module.require (module.js:498:17)
    at require (internal/module.js:20:19)
    at Object.<anonymous> (/Users/asuarez/Downloads/yarn-link-test/pkg-b/index.js:1:80)
    at Module._compile (module.js:571:32)
    at Object.Module._extensions..js (module.js:580:10)
    at Module.load (module.js:488:32)
    at tryModuleLoad (module.js:447:12)
    at Function.Module._load (module.js:439:3)
zsh: exit 1     node pkg-a
```
