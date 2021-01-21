# Build issue with thread-loader and ts-loader

This repo demonstrates a build error when using `thread-loader` in combination with `ts-loader` 8.0.8.

## Running it

- install modules `yarn install`
- try to build `yarn build`

An error should be displayed:

```
yarn run v1.22.5
warning package.json: No license field
$ webpack
[webpack-cli] Compilation finished
Hash: 544620ab4b9aa5be4c32
Version: webpack 4.44.2
Time: 564ms
Built at: 01/20/2021 5:32:04 PM
    Asset      Size  Chunks  Chunk Names
bundle.js  8.12 KiB       0  main
Entrypoint main = bundle.js
[0] ./src/app.ts 1.12 KiB {0} [built] [failed] [1 error]

ERROR in ./src/app.ts
Module build failed (from ./node_modules/thread-loader/dist/cjs.js):
Thread Loader (Worker 0)
Cannot read property 'hooks' of undefined
    at PoolWorker.fromErrorObj (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/thread-loader/dist/WorkerPool.js:344:12)
    at /home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/thread-loader/dist/WorkerPool.js:217:29
    at mapSeries (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/neo-async/async.js:3625:14)
    at PoolWorker.onWorkerMessage (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/thread-loader/dist/WorkerPool.js:171:34)
    at Object.initializeInstance (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/ts-loader/dist/instances.js:264:31)
    at successLoader (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/ts-loader/dist/index.js:26:17)
    at Object.loader (/home/cholzer/git/caseyjhol/tsloader-build-issue-with-thread-loader/node_modules/ts-loader/dist/index.js:23:5)
error Command failed with exit code 1.
```
